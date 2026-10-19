<script setup lang="ts">
import TheWelcome from '../components/TheWelcome.vue'
import HelloWorld from '../components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="home-intro">
      <HelloWorld msg="Hello World" />
    </div>
  </header>
  <main>
    <TheWelcome msg="Home" />
  </main>
</template>

<style scoped>
.home-intro {
  display: flex;
  justify-content: center;
}

.home-intro :deep(.greetings h1),
.home-intro :deep(.greetings h3) {
  text-align: center;
}
</style>
