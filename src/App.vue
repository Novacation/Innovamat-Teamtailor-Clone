<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div
    id="appContainer"
    class="relative w-full overflow-y-auto overflow-x-hidden">
    <RouterView />
  </div>
</template>

<style scoped>
@import url('./assets/reset.css');

#appContainer {
  min-height: 100vh;
}
</style>
