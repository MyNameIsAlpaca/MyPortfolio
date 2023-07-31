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

  <div class="container-card">
    <div class="img-container">
      <img class="card-img-top" :src="project.pic" alt="Card image cap">
    </div>
    <div class="info">
      <h5 class="card-title">{{ project.name }}</h5>
      <div class="language d-flex gap-2">
        <span class="single-language" v-for="language in project.language">{{ language }}</span>
      </div>
      <p class="card-text">{{ project.description }}</p>
    </div>
    <div class="button d-flex justify-content-between">
        <a :href="project.link" class="button"><i class="fa-solid fa-code"></i></a>
        <!-- <a href="#" class="button"><i class="fa-solid fa-eye"></i></a> -->
      </div>
  </div>

</template>

<style lang="scss">
.img-container{
  img{
    border-radius: 10px;
  }
}
.info{
  padding-top: 10px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  .card-title{
    text-align: center;
  }
  .card-text{
    max-height: 100px;
    overflow: auto;
  }
  .language{
    display: flex;
    flex-wrap: wrap;
  }
}
.button{
  padding-top: 10px;
}
.container-card{
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>