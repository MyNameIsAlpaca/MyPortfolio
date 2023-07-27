<script>

export default{
  name: 'AppProjectCard',

  data() {
    return {
     
    }
  },

  props: {

    project: Object,

  },

  created(){
  },

  methods: {
    
  }
}

</script>

<template>
  <div class="card">
    <img class="card-img-top" :src="project.pic" alt="Card image cap">
    <div class="type">
      {{ project.type }}
    </div>
    <div class="card-body">
      <h5 class="card-title">{{ project.name }}</h5>
      <div class="language">
        <span class="single-language" v-for="language in project.language">{{ language }}</span>
      </div>
      <p class="card-text">{{ project.description }}</p>
      <div class="button d-flex justify-content-between">
        <a :href="project.link" class="button"><i class="fa-solid fa-code"></i></a>
        <a href="#" class="button"><i class="fa-solid fa-eye"></i></a>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.card{
  width: 360px;
  position: relative;
  cursor:default;
}

.card-text{
  height: 130px;
  overflow: auto;
  margin: 5px 0px 5px 0px;
  padding: 5px;
  background-color: rgb(190, 190, 190);
  border-radius: 5px;
}
.language{
  display: flex;
  gap: 5px;
  overflow: auto;
  .single-language{
  font-size: 0.8em;
  background-color: rgba(20, 18, 156, 0.507);
  color: white;
  padding: 2px;
  border-radius: 10px;
  }
}
.type{
  position: absolute;
  background-color: rgba(0, 0, 0, 0.685);
  border-radius: 5px;
  padding: 2px;
  font-size: 0.8em;
  top: 10px;
  left: 10px;
  color: white;
}
</style>