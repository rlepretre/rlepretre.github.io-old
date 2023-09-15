<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <HelloWorld msg="Romain Leprêtre" />
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
  <div class="test"></div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);

}

@keyframes example {
  from {
    top: -10px;
    opacity: 100;
  }

  to {
    top: 100%;
    opacity: 0;
  }
}

.test {
  position: absolute;
  width: 5px;
  height: 5px;
  border-radius: 50%;
  top: 10%;
  left: 10%;
  background-color: #AFB3B7;
  animation-name: example;
  animation-iteration-count: infinite;
  animation-duration: 4s;
  filter: drop-shadow(0 0 20px #AFB3B7);
}
</style>
