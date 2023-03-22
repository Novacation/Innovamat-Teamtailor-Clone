<script setup>
defineProps({
  sidebarStatus: Boolean
})
</script>

<template>
  <nav
    class="absolute top-0 w-full h-full transition-all bg-slate-100 shadow-md drop-shadow-md z-40"
    :class="{ 'right-0': sidebarStatus, 'right-full': !sidebarStatus }">
    <p>Start</p>
    <p>Teams</p>
    <p>Locations</p>
    <p>Jobs</p>

    <div>
      <p>Employee</p>
      <p>Login</p>
    </div>

    <div>
      <p>Candidate</p>
      <p>Log in to Connect</p>
    </div>

    <div>
      <p>Homepage</p>
      <p>innovamat.com</p>
    </div>
  </nav>
</template>

<style scoped>
nav {
  min-height: 100vh;
}
</style>
