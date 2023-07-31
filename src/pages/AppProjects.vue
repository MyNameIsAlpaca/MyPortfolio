<script>
import projectsData from '../projects.json';
import AppProjectCard from '../components/AppProjectCard.vue';

import 'animate.css';

export default {
  name: "AppProjects",
  data() {
    return {
      projects: projectsData,
      activeIndex: 1,
    };
  },

  components: {
    AppProjectCard,
  },
};
</script>

<template>
  <div class="container">
    <h1 class="title">I miei progetti</h1>
    <div class="project-container container">
      <div class="single-project" v-for="project in projects" :key="project.id">
        <AppProjectCard :project="project"></AppProjectCard>
      </div>
    </div>
    <div class="container my-4">
      <div class="spinner-container">
        <div class="spinner">
        <div class="spinner">
          <div class="spinner">
            <div class="spinner">
              <div class="spinner">
                  <div class="spinner"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
     </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.title{
  font-size: 4em;
  padding-top: 70px;
  text-align: center;
  animation: slideInLeft;
  animation-duration: 2s;
}

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
  opacity: 0;
}

.single-project:nth-child(1){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 1s; 
}

.single-project:nth-child(2){
  animation: display 2s forwards;
  animation-duration: 2s;
  animation-delay: 2s; 
}
.single-project:nth-child(3){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 3s;
}

.single-project:nth-child(4){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 4s;
}
.single-project:nth-child(5){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 5s;
}

.single-project:nth-child(6){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 6s;
}
.single-project:nth-child(7){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 7s;
}

.single-project:nth-child(8){
  animation: display 2s forwards;
  animation-duration: 2s; 
  animation-delay: 8s;
}

@keyframes display {
  0% {
    opacity: 0;
  }
  100%{
    opacity: 1;
  }
}

@media screen and (max-width: 1200px) {
  .project-container{
    justify-content: center;
  }
}

@media screen and (max-width: 768px) {

  .title{
    font-size: 2em;
    padding: 10px;
    text-align: left;
  }
  .project-container{
    padding-left: 30px;
    padding-top: 10px;
    padding-bottom: 30px;
    gap: 30px;
  }
  .single-project{

  }
}

.spinner-container {
  width: 150px;
  height: 150px;
  position: relative;
  margin: 30px auto;
  overflow: hidden;
}

.spinner {
  position: absolute;
  width: calc(100% - 9.9px);
  height: calc(100% - 9.9px);
  border: 5px solid transparent;
  border-radius: 50%;
  border-top-color: #fff;
  animation: spin 5s cubic-bezier(0.17, 0.49, 0.96, 0.79) infinite;
}

@keyframes spin {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
</style>