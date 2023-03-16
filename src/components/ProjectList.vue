<script>
import ProjectCard from './ProjectCard.vue';
export default {
    name: 'ProjectList',
    components: { ProjectCard },
    props: { projects: Array }
};
</script>

<template>
    <main class="container">
        <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
    </main>
</template>