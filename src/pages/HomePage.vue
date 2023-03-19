<script>
import axios from 'axios';
import ProjectList from '../components/ProjectList.vue';

const apiBaseUrl = 'http://localhost:8000/api/';
export default {
    name: 'App',
    components: { ProjectList },
    data: () => ({
        projects: []
    }),
    methods: {
        callProjects() {
            axios.get(apiBaseUrl + 'project').then(res => {
                this.projects = res.data;
            })
        }
    },
    created() {
        this.callProjects();
    }
};
</script>

<template>
    <ProjectList :projects="projects" />
</template>