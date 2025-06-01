<script setup lang="ts">
import navBar from './components/nav-bar.vue'
import footerApp from './components/footer-app.vue';
</script>

<template>
  <navBar />
  <main>
    <RouterView />
  </main>
  <footerApp />
</template>

<style>
:root {
  --bg-color: linear-gradient(to right, #363636 0%, black 100%);
}
.bg-blue-color{
  background: var(--bg-color);
}
.border-blue{
  border: 1px solid var(--bg-color);
}
body {
  scroll-behavior: smooth;
  background: var(--bg-color);
  backdrop-filter: blur(12px);
}
</style>
