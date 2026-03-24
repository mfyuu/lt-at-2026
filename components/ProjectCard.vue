<script setup lang="ts">
defineProps<{
  name: string
  users: string[]
}>()
</script>

<template>
  <div class="flex items-center gap-4">
    <span>{{ name }}</span>
    <AvatarStack :users="users" />
  </div>
</template>
