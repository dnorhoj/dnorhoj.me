<script setup>
// TODO: Hover/click/more info
defineProps({
    icon: String,
    title: String
})
</script>

<template>
    <div class="container">
        <div class="separator">
            <div class="icon">
                <i :class="`bi bi-${icon}`"></i>
            </div>
        </div>
        <span class="title">{{ title }}</span>
    </div>
</template>

<style scoped>
.container {
    @apply bg-white rounded-lg w-64 h-14 md:h-20 flex items-center drop-shadow-lg text-neutral-800 overflow-hidden;
}

.icon {
    @apply p-3 overflow-hidden inline-block text-2xl
}

.separator {
    @apply h-full drop-shadow-lg rounded-r-2xl flex items-center mr-3 bg-neutral-800 text-white
}

.title {
    @apply text-xl font-bold
}
</style>