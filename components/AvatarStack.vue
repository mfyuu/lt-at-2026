<script setup lang="ts">
defineProps<{
  users: string[]
}>()
</script>

<template>
  <div
    class="relative h-6"
    :style="{ width: `${(users.length - 1) * 16 + 24}px` }"
  >
    <img
      v-for="(user, i) in users"
      :key="user"
      :src="`https://github.com/${user}.png`"
      height="24"
      width="24"
      class="absolute top-0 rounded-full border"
      :style="{
        left: `${i * 16}px`,
        zIndex: (users.length - i) * 10,
      }"
    />
  </div>
</template>
