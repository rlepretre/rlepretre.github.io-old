<script setup>
import Hero from './components/Hero.vue'
import Snow from './components/Snow.vue'
import { ref } from "vue";

let toggleSnow = ref(true);
</script>

<template>
  <div class="main">
    <Hero msg="Romain Leprêtre" />
    <div class="toggles">
      <button @click="toggleSnow = !toggleSnow">
        <font-awesome-icon icon="fa-regular fa-snowflake"></font-awesome-icon>
      </button>
    </div>
  </div>
  <Snow :snowing=toggleSnow />
</template>

<style scoped>
.main{
  display: flex;
  align-items: center;
  justify-content: center;
}
.toggles {
  align-self: flex-start;
}
</style>
