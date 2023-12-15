<script setup>
defineProps({
    snowing: Boolean,
})
</script>

<template>
    <div v-show="snowing">
        <div v-for="i in 100" class="snow fall"
            :style="{ animationDelay: `${Math.random() * 10}s`, left: `${Math.random() * 98}%` }"></div>
    </div>
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
    background-color: var(--lightGray);
    will-change: filter;
    transition: filter 300ms;
}

.fall {
    animation-name: drop;
    animation-duration: 4s;
    animation-iteration-count: infinite;
    animation-timing-function: cubic-bezier(.5, 0, 1, .5);
    filter: drop-shadow(0 0 10px var(--lightGray));
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
    .snow {
        background-color: var(--darkBlue);
    }

    .fall {
        filter: drop-shadow(0 0 10px var(--darkBlue));
    }
}
</style>
