<script setup lang="ts">
defineProps<{
  src: string;
  caption?: string;
}>();
</script>

<template>
  <div class="inline-block relative rounded-lg overflow-hidden shadow-lg">
    <div class="w-100 h-72 overflow-hidden bg-gray-100">
      <img
        :src="src"
        class="w-full h-full object-cover"
      />
    </div>
    <div v-if="caption" class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent px-4">
      <p class="text-white text-sm font-medium">
        {{ caption }}
      </p>
    </div>
  </div>
</template>
