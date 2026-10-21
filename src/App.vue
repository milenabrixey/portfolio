<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
import PlasmaWave from './components/PlasmaWave/PlasmaWave.vue'
</script>

<template>
  <div class="isolate min-h-screen">
    <div class="pointer-events-none fixed inset-0 z-0" aria-hidden="true">
      <PlasmaWave
        :colors="['#27FF64', '#7CFF67']"
        :speed1="0.05"
        :speed2="0.05"
        :focal-length="0.8"
        :bend1="1"
        :bend2="0.5"
        :dir2="1.0"
        :rotation-deg="30"
      />
    </div>

    <div class="relative z-10 flex h-[calc(100dvh-4rem)] min-h-0 flex-col">
      <header class="shrink-0">
        <NavBar />
      </header>
      <RouterView />
    </div>
  </div>
</template>
