<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div id="appContainer" class="relative w-full overflow-hidden">
    <RouterView />
  </div>
</template>

<style scoped>
@import url('./assets/reset.css');
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@300;400&display=swap');

#appContainer {
  min-height: 100vh;
}
</style>
