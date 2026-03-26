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
}>();

const size = computed(() => props.size ?? 280);
const center = computed(() => size.value / 2);
const radius = computed(() => size.value / 2 - 10);

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
    const labelRadius = radius.value * 0.65;
    const labelX = center.value + labelRadius * Math.cos(midRad);
    const labelY = center.value + labelRadius * Math.sin(midRad);

    return {
      ...segment,
      d: `M ${center.value} ${center.value} L ${x1} ${y1} A ${radius.value} ${radius.value} 0 ${largeArc} 1 ${x2} ${y2} Z`,
      labelX,
      labelY,
      showLabel: segment.value >= 5,
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
      <template v-for="(p, i) in paths" :key="'label-' + i">
        <text
          v-if="p.showLabel"
          :x="p.labelX"
          :y="p.labelY"
          text-anchor="middle"
          dominant-baseline="central"
          fill="white"
          font-size="4"
          font-weight="bold"
          class="drop-shadow"
        >
          {{ p.value }}%
        </text>
      </template>
    </svg>
    <div class="flex flex-col justify-between h-full py-2" style="min-height: 280px">
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
          <span class="text-gray-400 ml-1">{{ s.value }}%</span></span
        >
      </div>
    </div>
  </div>
</template>
