<script setup>
import { ref } from 'vue';
defineProps({
    title: String,
    pages: Array
})

let shown = ref(false)
</script>

<template>
    <div v-show="!shown" @click="shown = !shown" class="nav-extender">
        <i class="bi bi-list"></i>
    </div>
    <div v-show="shown" class="nav">
        <div class="nav-title">
            <i class="bi bi-list close" @click="shown = !shown"></i>
            <span>{{ title }}</span>
            <div class="w-10"></div>
        </div>
        <hr />
        <div class="nav-content" @click="shown = !shown">
            <a class="nav-item" href="#front">Frontpage</a>
            <a class="nav-item" href="#projects">Projects</a>
            <a class="nav-item" href="#skills">Skills</a>
            <a class="nav-item" href="#contact">Contact</a>
        </div>
    </div>
</template>

<style scoped>
.nav-extender {
    @apply fixed m-5 w-10 h-10 bg-white rounded-lg z-10 flex justify-center items-center cursor-pointer hover:bg-neutral-300 drop-shadow-xl
}

.nav {
    @apply fixed m-5 z-20 drop-shadow-xl bg-white rounded-lg overflow-hidden w-[calc(100%-2.5rem)] md:w-auto
}

.nav-title {
    @apply flex justify-between
}

.nav-title>* {
    @apply p-2 font-bold
}

.nav-title>.close {
    @apply hover:bg-neutral-300 rounded-lg w-10 h-10 text-center cursor-pointer
}

.nav-content {
    @apply flex flex-col items-center flex-grow
}

.nav-content>hr {
    @apply w-full
}

.nav-item {
    @apply p-1 hover:bg-neutral-800 hover:text-white w-full text-center
}

.nav-item>a {
    @apply block h-full
}

.title {
    @apply font-bold
}
</style>