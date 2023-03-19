<script>
import axios from 'axios';
import ProjectCard from '../components/ProjectCard.vue';

const apiBaseUrl = 'http://localhost:8000/api/';
export default {
    name: 'ShowPage',
    components: { ProjectCard },
    data: () => ({
        project: null,
    }),
    methods: {
        callProjects() {
            axios.get(endpoint).then(res => {
                this.projects = res.data;
            }).catch(err => {
                console.log(err);
            })
        }
    },
    created() {
        this.callProjects();
    }
};
</script>

<template>
    <!-- <AppHeader /> -->
    <main class="container">
        <ProjectCard :projects="projects" />
    </main>
</template>