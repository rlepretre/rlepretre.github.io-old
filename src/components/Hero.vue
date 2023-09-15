<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>
  <div>
    <h2>
      <a href="/" target="_blank">
        Home
      </a>
      <span>|</span>
      <a href="/" target="_blank">
        About
      </a>
      <span>|</span>
      <a href="/" target="_blank">
        Projects
      </a>
    </h2>
  </div>
</template>

<style scoped>
h1 {
  font-size: 3.2em;
  line-height: 1.1;
}

h2 {
  font-size: 1.7em;
  line-height: 1.1;
}

a {
  font-weight: 500;
  color: var(--lightBlue);
  text-decoration: inherit;
}

a:hover {
  color: var(--blue);
}

@media (prefers-color-scheme: light) {
  a {
    font-weight: 500;
    color: var(--blue);
    text-decoration: inherit;
  }

  a:hover {
    color: var(--lightBlue);
  }
}
</style>
