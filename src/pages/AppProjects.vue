<script>
import projectsData from '../projects.json';
import AppProjectCard from '../components/AppProjectCard.vue';

export default {
  name: "AppProjects",
  data() {
    return {
      projects: projectsData,
      activeIndex: 1,
    };
  },
  created() {
  },
  methods: {
  },
  components: {
    AppProjectCard,
  },
};
</script>

<template>
  <div class="project-container container">
    <div v-for="project in projects" :key="project.id">
      <AppProjectCard :project="project"></AppProjectCard>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.project-container{
  padding-top: 70px;
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
</style>
