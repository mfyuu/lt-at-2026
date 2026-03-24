<script setup lang="ts">
defineProps<{
  projects: Array<{ name: string; users: string[] }>
}>()
</script>

<template>
  <div class="space-y-4">
    <slot name="header" />
    <ProjectCard
      v-for="p in projects"
      :key="p.name"
      :name="p.name"
      :users="p.users"
    />
  </div>
</template>
