<script setup>
defineProps({
  sidebarStatus: Boolean
})
</script>

<template>
  <nav
    class="absolute top-0 w-full h-full transition-all bg-slate-100 shadow-md drop-shadow-md z-40 text-neutral-800 overflow-y-auto overflow-x-hidden"
    :class="{ 'right-0': sidebarStatus, 'right-full': !sidebarStatus }">
    <ul class="w-full mt-20 text-[24px] font-bold">
      <li class="py-3 px-8"><p>Start</p></li>
      <li class="py-3 px-8"><p>Teams</p></li>
      <li class="py-3 px-8"><p>Locations</p></li>
      <li class="py-3 px-8"><p>Jobs</p></li>
    </ul>

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
