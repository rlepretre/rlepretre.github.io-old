<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
const snowFlake = ref(null);
onMounted(() => {
    console.log(snowFlake);
})

// var time = Math.random();
// var red = document.querySelector('#fall');
// red.style.setProperty('--animation-time', time +'s');
</script>

<template>
    <div v-for="i in 100" ref="snowFlake" class="snow fall"
        :style="{ animationDelay: `${Math.random() * 10}s`, left: `${Math.random() * 98}%` }"></div>
</template>

<style scoped>
:root {
    --animation-delay: 2s;
}

.snow {
    position: absolute;
    width: 5px;
    height: 5px;
    border-radius: 50%;
    top: -20px;
    background-color: var(--darkerBlue);
    will-change: filter;
    transition: filter 300ms;
}

.fall {
    animation-name: drop;
    animation-duration: 4s;
    animation-iteration-count: infinite;
    animation-timing-function: cubic-bezier(.5, 0, 1, .5);
    filter: drop-shadow(0 0 10px var(--darkBlue));
}

@keyframes drop {
    from {
        top: -10px;
        opacity: 90;
    }

    to {
        top: 99%;
        opacity: 0;
    }
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
