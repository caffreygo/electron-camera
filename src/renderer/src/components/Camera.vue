<script setup lang="ts">
import { onMounted } from 'vue'
// const devices = await navigator.mediaDevices.enumerateDevices()

onMounted(() => {
  const constraints = {
    audio: true,
    video: true
  }

  const playerEl: HTMLVideoElement = document.querySelector('#player')!

  navigator.mediaDevices.getUserMedia(constraints).then(function (stream) {
    playerEl.srcObject = stream
    playerEl.play()
  })
})
</script>

<template>
  <video id="player"></video>
</template>

<style lang="scss" scoped>
main {
  width: 100vw;
  height: 100vh;

  video {
    display: block;
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
}
</style>
