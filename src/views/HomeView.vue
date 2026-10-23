<script setup lang="ts">
import FoldText from '@/components/FoldText/FoldText.vue'
import GlassSurface from '@/components/GlassSurface/GlassSurface.vue';
import GradientText from '@/components/GradientText/GradientText.vue'
</script>

<template>
  <main class="relative flex min-h-0 flex-1 items-center justify-center px-4">
    <div class="relative">
      <h1
        class="absolute bottom-full left-0 mb-8 flex w-max max-w-[calc(100vw-2rem)] flex-col items-start gap-1 text-left text-4xl leading-tight sm:text-5xl"
      >
        <span>Hello, my name is</span>
        <GradientText
          :colors="['var(--custom-color-primary)', 'var(--custom-color-secondary)', 'var(--custom-color-secondary)']"
          :animation-speed="3"
          :show-border="false"
          class-name="!mx-0"
        >
          Milena Brixey
        </GradientText>
        <span>and I'm a</span>
      </h1>
      <GlassSurface
        width="auto"
        height="auto"
        :border-radius="20"
        :background-opacity="0"
        content-padding="0.5rem 0"
        :style="{
          background: 'transparent',
          backdropFilter: 'blur(12px)',
          WebkitBackdropFilter: 'blur(12px)',
          border: 'none',
          boxShadow: 'none'
        }"
      >
        <FoldText
          text="Software Developer"
          split-by="char"
          hinge="top"
          trigger="mount"
          :duration="0.65"
          :stagger="0.045"
          ease="power3.out"
          :perspective="700"
          :crease-shading="0.55"
          :font-size="'clamp(2rem, 7vw, 5rem)'"
          :font-weight="800"
          class="gradient-text"
        />
      </GlassSurface>
    </div>
  </main>
</template>
