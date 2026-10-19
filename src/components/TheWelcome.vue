<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
defineProps<{
  msg: string
}>()
</script>

<template>
  <WelcomeItem>
    <template #heading>{{ msg }}</template>

    This is a page.
  </WelcomeItem>
</template>
