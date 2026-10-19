<script setup lang="ts">
import { computed } from 'vue'
import { useRoute, useRouter } from 'vue-router'
import JellyRadio from '@/components/JellyRadio/JellyRadio.vue'

const router = useRouter()
const route = useRoute()

const destinations = [
  { value: 'Home', label: 'Home', path: '/' },
  { value: 'About', label: 'About', path: '/about' },
  { value: 'Skills', label: 'Skills', path: '/skills' },
  { value: 'Contact', label: 'Contact', path: '/contact' },
]

const selectedPage = computed(() => {
  return destinations.find((item) => item.path === route.path)?.value ?? 'Home'
})

function navigateToPage(value: string) {
  const destination = destinations.find((item) => item.value === value)
  if (destination && destination.path !== route.path) {
    router.push(destination.path)
  }
}
</script>

<template>
  <nav aria-label="Main navigation">
    <JellyRadio
      :items="destinations.map(({ value, label }) => ({ value, label }))"
      :value="selectedPage"
      aria-label="Pages"
      @change="navigateToPage"
    />
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  justify-content: center;
  width: 100%;
  margin-bottom: 1rem;
}
</style>
