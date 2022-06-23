<script setup>
import Project from '../components/Project.vue';
</script>

<template>
    <div class="projects" id="projects">
        <h1 class="title">Projects</h1>
        <div class="project-container">
            <Project title="AntiRickRoll" icon="globe" description="Browser extension that blocks Rickrolls!"
                lang="JS, HTML">
                <a href="https://antirickroll.com/" aria-label="AntiRickRoll website" target="_blank">
                    <i class="bi bi-globe2"></i>
                </a>
                <a href="https://github.com/dnorhoj/AntiRickRoll" aria-label="AntiRickRoll GitHub Repository" target="_blank">
                    <i class="bi bi-github"></i>
                </a>
            </Project>
            <Project title="Lectio.py" icon="filetype-py"
                description="Python library which interfaces the Lectio website through HTTP requests." lang="Python">
                <a href="https://pypi.org/project/lectio.py/" aria-label="Lectio.py website" target="_blank">
                    <i class="bi bi-globe2"></i>
                </a>
                <a href="https://github.com/dnorhoj/lectio.py" aria-label="Lectio.py GitHub Repository" target="_blank">
                    <i class="bi bi-github"></i>
                </a>
            </Project>
            <Project title="Unnamed Discord Bot" icon="filetype-py" description="Unnamed general purpose discord bot."
                lang="Python">
                <a href="https://github.com/dnorhoj/unnameddiscordbot" aria-label="Unnamed Discord Bot GitHub Repository" target="_blank">
                    <i class="bi bi-github"></i>
                </a>
            </Project>
        </div>
    </div>
</template>

<style scoped>
.projects {
    @apply relative flex justify-center items-center flex-col snap-center h-screen
}

.title {
    @apply inline font-bold text-white drop-shadow-lg text-center text-3xl md:text-5xl;
}

.project-container {
    @apply grid md:grid-cols-2 lg:grid-cols-3 justify-center border-white border-t-2 mt-4 p-3 max-h-[75vh] overflow-scroll
}

.project-container>* {
    @apply m-2;
}
</style>