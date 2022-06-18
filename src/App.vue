<script setup>
import Front from './pages/Front.vue';
import Projects from './pages/Projects.vue';
import Skills from './pages/Skills.vue';
import Contact from './pages/Contact.vue';
</script>

<template>
  <!-- TODO: navbar / CTRL K ting -->
  <div tabindex="0" class="main">
    <Front />
    <Projects />
    <Skills />
    <Contact />
  </div>
</template>

<style scoped>
.main {
  @apply snap-x overflow-y-scroll h-screen scroll-smooth bg-gradient-to-br from-red-500 to-indigo-600;
}

.main > div {
    @apply snap-center h-screen
}

</style>