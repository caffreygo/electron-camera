<script setup lang="ts">
import Camera from './components/Camera.vue'
</script>

<template>
  <suspense>
    <main>
      <Camera />
    </main>
  </suspense>
</template>

<style scoped>
main {
  width: 100vw;
  height: 100vh;
}
</style>
