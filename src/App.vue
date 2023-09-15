<script setup>
import Hero from './components/Hero.vue'
import Snow from './components/Snow.vue'
</script>

<template>
  <Hero msg="Romain Leprêtre" />
  <Snow v-show="toggleSnow" />
</template>

<style scoped>

</style>
