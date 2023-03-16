<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import ProjectList from './components/ProjectList.vue';
const apiBaseUrl = 'http://localhost:8000/api/';
export default {
  name: 'App',
  components: { AppHeader, ProjectList },
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
  <AppHeader />
  <main class="container">
    <ProjectList :projects="projects" />
  </main>
</template>