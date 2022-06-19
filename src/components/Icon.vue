<script setup>
defineProps({
    icon: String,
    href: String,
    target: String
})
</script>

<template>
    <a class="icon" :href="href" :target="target">
        <i :class="`bi bi-${icon}`"></i>
    </a>
</template>

<style scoped>
.icon {
  @apply p-3 mx-1 bg-white rounded-xl drop-shadow-lg hover:-translate-y-1 transition-all hover:drop-shadow-xl cursor-pointer
}

.icon i {
  @apply text-neutral-700 text-4xl
}

</style>