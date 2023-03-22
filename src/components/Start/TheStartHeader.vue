<script setup>
import { ref, computed } from 'vue'
import Sidebar from '../Global/Sidebar.vue'

const sidebarStatus = ref(false)

const toggleSidebar = () => {
  sidebarStatus.value = !sidebarStatus.value
  let bodyOverflow = document.getElementsByTagName('body')[0].style.overflow
  if (bodyOverflow == 'hidden') {
    document.getElementsByTagName('body')[0].style.overflow = 'auto'
  } else document.getElementsByTagName('body')[0].style.overflow = 'hidden'
}

const menuFirstChildHeight = computed(() => {
  if (!sidebarStatus.value) {
    return '0px'
  } else return '10px'
})

const menuFirstChildRotateZ = computed(() => {
  if (!sidebarStatus.value) {
    return '0deg'
  } else return '45deg'
})

const menuLastChildHeight = computed(() => {
  if (!sidebarStatus.value) {
    return '0px'
  } else return '-6px'
})

const menuLastChildRotateZ = computed(() => {
  if (!sidebarStatus.value) {
    return '0deg'
  } else return '-45deg'
})

const menuChildsColor = computed(() => {
  if (!sidebarStatus.value) {
    return '255,255,255'
  } else return '51, 51, 51'
})
</script>

<template>
  <header class="relative flex flex-col justify-start w-full p-5">
    <video
      class="hidden sm:block absolute inset-0 object-cover w-full h-full"
      preload="none"
      loop="loop"
      muted="muted"
      autoplay="autoplay"
      playsinline="playsinline">
      <source
        src="https://videos.teamtailor-cdn.com/tt-videos-production/uploads_converted/cover_large/f68e650a759d4ed29b0123e6b2203a75cab1c1e5.mp4"
        type="video/mp4" />

      <source
        src="https://videos.teamtailor-cdn.com/tt-videos-production/uploads_converted/cover_large/f68e650a759d4ed29b0123e6b2203a75cab1c1e5.webm"
        type="video/webm" />
    </video>
    <img
      src="https://images.teamtailor-cdn.com/images/s3/teamtailor-production/logotype-v3/image_uploads/c7db2a8c-d905-4503-ae78-352117777c0c/original.png"
      alt="Logo de Innovamat"
      class="w-44 self-center z-40" />
    <div
      @click="toggleSidebar"
      class="burgerMenu flex flex-col justify-between items-center cursor-pointer"
      :class="{ 'z-50': sidebarStatus }">
      <div></div>
      <div v-show="!sidebarStatus"></div>
      <div></div>
    </div>
    <Sidebar :sidebar-status="sidebarStatus" />

    <div
      class="w-full relative text-white flex flex-col self-center justify-center items-center pt-[80px] pb-14 sm:pt-[90px] md:max-w-[75%] lg:py-0">
      <h1 class="text-center max-w-[430px] text-[50px] font-bold">
        Welcome to Innovamat
      </h1>

      <div
        class="flex flex-col justify-center items-center w-full mt-8 sm:flex-row sm:gap-x-20">
        <button
          class="flex flex-col justify-center items-center headerBtns w-52 text-sm font-bold mt-4 py-4 px-8 shadow-md drop-shadow-md rounded-md">
          <a href="#">Connect</a>
        </button>

        <button
          class="flex flex-col justify-center items-center headerBtns w-52 text-sm font-bold mt-4 py-4 px-8 shadow-md drop-shadow-md rounded-md">
          <a href="#">Job Openings</a>
        </button>
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  background-image: url('../../assets/imgs/mobile_bg.png');
  background-repeat: no-repeat;
  background-position: 50%;
  background-attachment: local;
  background-size: cover;
  background-color: rgb(51, 51, 51);
}

header .burgerMenu {
  position: absolute;
  top: 35px;
  left: 20px;
  width: 24px;
  height: 18px;
}

.burgerMenu div {
  position: relative;
  top: 0;
  width: 100%;
  height: 2px;
  background-color: rgb(v-bind(menuChildsColor));
  transition: 0.1s ease transform, 0.1s ease top, 0.1s ease width,
    0.1s ease right;
  border-radius: 2px;
}

.burgerMenu div:first-child {
  top: v-bind(menuFirstChildHeight);
  transform: rotateZ(v-bind(menuFirstChildRotateZ));
}

.burgerMenu div:last-child {
  top: v-bind(menuLastChildHeight);
  transform: rotateZ(v-bind(menuLastChildRotateZ));
}

.headerBtns {
  background-color: rgb(36, 36, 36);
}
</style>
