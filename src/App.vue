<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div id="appContainer" class="relative w-full overflow-hidden">
    <RouterView />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@300;400&display=swap');

#appContainer {
  min-height: 100vh;
}

.floatFx {
  animation: float 3s ease-in-out infinite;
}

.floatFxSlower {
  animation: float 5s ease-in-out infinite;
}

@keyframes float {
  0% {
    transform: translatey(0px);
  }

  50% {
    transform: translatey(-10px);
  }

  100% {
    transform: translatey(0px);
  }
}
</style>
