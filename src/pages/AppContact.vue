<script>

export default {
  name: "AppContact",
  data() {
    return {

    };
  },
  created() {
  
  },
  methods: {
    
  },
  components: {
  },
};
</script>

<template>
  <div class="background">
    <div class="bg"></div>
    <div class="bg bg2"></div>
    <div class="bg bg3"></div>
  </div>
</template>

<style lang="scss" scoped>

.background{
  .bg {
  animation:slide 6s ease-in-out infinite alternate;
  background-image: linear-gradient(-60deg, #231F20 50%, #ca691a 50%);
  bottom:0;
  left:-50%;
  opacity:.5;
  position:fixed;
  right:-50%;
  top:0;
  z-index:-1;
}

.bg2 {
  animation-direction:alternate-reverse;
  animation-duration:8s;
}

.bg3 {
  animation-duration:10s;
}


@keyframes slide {
  0% {
    transform:translateX(-25%);
  }
  100% {
    transform:translateX(25%);
  }
}
}

</style>