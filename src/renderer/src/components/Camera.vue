<script setup lang="ts">
const devices = await navigator.mediaDevices.enumerateDevices()
</script>

<template>
  <main>
    {{ devices }}
  </main>
</template>
