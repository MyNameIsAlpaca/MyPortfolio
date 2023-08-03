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
<a :href="project.link">
  <div class="container-card">
    <div class="img-container">
      <div class="bookmarkRibbon"><span class="type" style="color:white;position: relative;top: -9px;">{{ project.type }}</span></div>
      <img class="card-img-top" :src="project.pic" alt="Card image cap">
    </div>
    <div class="info">
      <h5 class="card-title">{{ project.name }}</h5>
      <hr class="mx-5">
      <p class="card-text">{{ project.description }}</p>
    </div>
    <div class="button d-flex justify-content-between p-2">
      <div class="language d-flex gap-2 flex-wrap">
        <span class="single-language" v-for="language in project.language">{{ language }}</span>
      </div>
    </div>
  </div>
</a>

</template>


<style lang="scss">

a {
     text-decoration: none;
     color: white;
}

.bookmarkRibbon {
        width: 105px;
        height: 0;
        border-bottom: 20px solid #07899b;
        border-top: 20px solid #220247;
        border-left: 15px solid transparent;
        margin-bottom: 20px;
        font-weight:700;
        position: absolute;
        right: -5px;
        top: -5px;
        border-radius: 0px 10px 0px 0px;
        display: flex;
        justify-content: center;
    }

.img-container{
  position: relative;
  .type{
    font-size: 0.8em;
  }
}


.info{
  padding-top: 10px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 10px;
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
  background-color: rgba(38, 53, 24, 0.479);
  max-width: 500px;
  border: 5px solid white;
  border-radius: 10px;
}
</style>