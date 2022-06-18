<script setup>
import Skill from '../components/Skill.vue';
</script>

<template>
  <div class="skills" id="skills">
    <h1 class="title">Skills</h1>
    <div class="skill-container">
      <Skill icon="file-earmark-binary" title="Cybersecurity" />
      <Skill icon="gear" title="Software development" />
      <Skill icon="globe" title="Web development" />
      <Skill icon="filetype-py" title="Python" />
      <Skill icon="filetype-js" title="JavaScript" />
      <Skill icon="filetype-html" title="HTML/CSS" />
      <Skill icon="git" title="Git" />
      <Skill icon="hdd-stack" title="Linux" />
      <Skill icon="server" title="Database" />
    </div>
  </div>
</template>

<style scoped>
.skills {
  @apply relative flex justify-center items-center
  flex-col lg:flex-row
}

.title {
  @apply inline font-bold text-white drop-shadow-lg text-center text-3xl md:text-5xl;
}

.skill-container {
  @apply grid md:grid-cols-2 lg:grid-cols-3 justify-center border-white border-t-2 mt-4 p-3
  max-h-[75vh] overflow-scroll lg:border-t-0 lg:border-l-2 lg:mt-0 lg:ml-4
}

.skill-container > * {
  @apply m-2;
}
</style>