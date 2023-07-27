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
    <div class="single-project" v-for="project in projects" :key="project.id">
      <AppProjectCard :project="project"></AppProjectCard>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.project-container{
  padding-top: 100px;
  display: flex;
  flex-wrap: wrap;
  gap: 100px;
  justify-content: space-between;
}

.single-project{
  max-width: 500px;
  border: 5px solid white;
  border-radius: 10px;
  padding: 10px;
  background-color: rgb(0, 0, 0);
}

@media screen and (max-width: 768px) {
  .project-container{
    padding-left: 30px;
    padding-top: 10px;
  }
  .single-project{

  }
}
</style>
