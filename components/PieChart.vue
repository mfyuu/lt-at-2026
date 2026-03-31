<script setup lang="ts">
import { computed } from "vue";

interface Segment {
  label: string;
  value: number;
  color: string;
}

const props = defineProps<{
  segments: Segment[];
  size?: number;
  unit?: string;
  hideLegend?: boolean;
}>();

const chartSize = computed(() => props.size ?? 280);
const margin = computed(() => (props.unit === "h" ? 40 : 0));
const size = computed(() => chartSize.value + margin.value * 2);
const center = computed(() => size.value / 2);
const radius = computed(() => chartSize.value / 2 - 10);

const clockMarks = computed(() => {
  if (props.unit !== "h") return [];
  const total = props.segments.reduce((sum, s) => sum + s.value, 0);
  const marks = [];
  for (let h = 0; h < total; h++) {
    const angle = -90 + (h / total) * 360;
    const rad = (angle * Math.PI) / 180;
    const labelR = radius.value + 16;
    marks.push({
      hour: h,
      x: center.value + labelR * Math.cos(rad),
      y: center.value + labelR * Math.sin(rad),
    });
  }
  return marks;
});

const paths = computed(() => {
  const total = props.segments.reduce((sum, s) => sum + s.value, 0);
  let currentAngle = -90;
  return props.segments.map((segment) => {
    const angle = (segment.value / total) * 360;
    const startAngle = currentAngle;
    const endAngle = currentAngle + angle;
    currentAngle = endAngle;

    const startRad = (startAngle * Math.PI) / 180;
    const endRad = (endAngle * Math.PI) / 180;

    const x1 = center.value + radius.value * Math.cos(startRad);
    const y1 = center.value + radius.value * Math.sin(startRad);
    const x2 = center.value + radius.value * Math.cos(endRad);
    const y2 = center.value + radius.value * Math.sin(endRad);

    const largeArc = angle > 180 ? 1 : 0;

    const midRad = ((startAngle + endAngle) / 2) * (Math.PI / 180);
    const isSmall = angle < 10;
    const labelRadius = isSmall ? radius.value + 30 : radius.value * 0.65;
    const labelX = center.value + labelRadius * Math.cos(midRad);
    const labelY = center.value + labelRadius * Math.sin(midRad);

    const leaderStart = {
      x: center.value + (radius.value * 0.85) * Math.cos(midRad),
      y: center.value + (radius.value * 0.85) * Math.sin(midRad),
    };
    const leaderEnd = {
      x: center.value + (radius.value + 20) * Math.cos(midRad),
      y: center.value + (radius.value + 20) * Math.sin(midRad),
    };

    return {
      ...segment,
      d: `M ${center.value} ${center.value} L ${x1} ${y1} A ${radius.value} ${radius.value} 0 ${largeArc} 1 ${x2} ${y2} Z`,
      labelX,
      labelY,
      fontSize: 10,
      isSmall,
      leaderStart,
      leaderEnd,
      textAnchor: isSmall ? (Math.cos(midRad) >= 0 ? 'start' : 'end') : 'middle',
    };
  });
});
</script>

<template>
  <div class="flex items-center gap-8">
    <svg :width="size" :height="size" class="drop-shadow-lg">
      <path
        v-for="(p, i) in paths"
        :key="i"
        :d="p.d"
        :fill="p.color"
        stroke="white"
        stroke-width="2"
        class="transition-all duration-500"
      />
      <text
        v-for="m in clockMarks"
        :key="'clock-' + m.hour"
        :x="m.x"
        :y="m.y"
        text-anchor="middle"
        dominant-baseline="central"
        fill="currentColor"
        font-size="4"
        opacity="0.5"
      >
        {{ m.hour }}
      </text>
      <template v-for="(p, i) in paths" :key="'label-' + i">
        <line
          v-if="p.isSmall"
          :x1="p.leaderStart.x"
          :y1="p.leaderStart.y"
          :x2="p.leaderEnd.x"
          :y2="p.leaderEnd.y"
          stroke="currentColor"
          stroke-width="0.5"
          opacity="0.6"
        />
        <text
          :x="p.labelX"
          :y="p.labelY"
          :text-anchor="p.textAnchor"
          dominant-baseline="central"
          :fill="p.isSmall ? 'currentColor' : 'white'"
          :font-size="p.fontSize"
          :font-weight="p.isSmall ? 'normal' : 'bold'"
          :class="p.isSmall ? '' : 'drop-shadow'"
        >
          {{ p.label }}
        </text>
      </template>
    </svg>
    <div v-if="!hideLegend" class="flex flex-col justify-between h-full py-2" style="min-height: 280px">
      <div
        v-for="(s, i) in segments"
        :key="i"
        class="flex items-center gap-3"
      >
        <span
          class="inline-block w-5 h-5 rounded-sm shrink-0"
          :style="{ backgroundColor: s.color }"
        />
        <span class="text-base whitespace-nowrap"
          >{{ s.label }}
          <span class="text-gray-400 ml-1">{{ s.value }}{{ unit ?? '%' }}</span></span
        >
      </div>
    </div>
    <slot v-else />
  </div>
</template>
