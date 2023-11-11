<template lang="pug">
video(autoplay loop muted class="bgvideo")
  source(src="./assets/first-screen.mp4" type="video/mp4")
div(class="log")
  Login
</template>

<script setup>
import Login from "./components/Login.vue";
</script>

<style scoped>
.bgvideo {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: -9999;
}

.log {
  position: relative;
  top: 116px;
}
</style>
