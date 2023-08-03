<script>

import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/css';

import 'swiper/css/effect-creative';

import '../style.scss';

import { EffectCreative } from 'swiper/modules';

export default {
  name: "AppHome",
  data() {
    return {

    };
  },


  components: {
    Swiper,
    SwiperSlide,
    
  },
  setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [EffectCreative],
      };
    },
};
</script>

<template>
  <div class="background">
    <div class="bg"></div>
    <div class="bg bg2"></div>
    <div class="bg bg3"></div>
    
    <div class="main-container">
      <div class="image-container">
        <img src="/img/curriculum_foto_def.jpg" alt="Immagine di profilo">
      </div>
      <h3 class="pt-3"><em>Conoscenze:</em></h3>
      <swiper :grabCursor="true" :effect="'creative'" :creativeEffect="{ prev: { shadow: true, translate: [0, 0, -400],}, next: { translate: ['100%', 0, 0],},}" :modules="modules" class="mySwiper">
        <swiper-slide><i class="fa-brands fa-html5"></i><span class="swiper_name">Html</span> <em class="swipe_arrow">swipe <i class="fa-solid fa-arrow-right"></i></em></swiper-slide>
        <swiper-slide><i class="fa-brands fa-css3-alt"></i><span class="swiper_name">Css</span></swiper-slide>
        <swiper-slide><i class="fa-brands fa-js"></i><span class="swiper_name">Javascript</span></swiper-slide>
        <swiper-slide><i class="fa-brands fa-bootstrap"></i><span class="swiper_name">Bootstrap</span></swiper-slide>
        <swiper-slide><i class="fa-brands fa-vuejs"></i><span class="swiper_name">VueJs</span></swiper-slide>
        <swiper-slide><i class="fa-brands fa-php"></i><span class="swiper_name">Php</span></swiper-slide>
        <swiper-slide><i class="fa-brands fa-laravel"></i><span class="swiper_name">Laravel</span></swiper-slide>
      </swiper> 
      <div class="info-section">
            <h1 id="name">Gabriele Saragosa</h1>
            <span id="sub" class="sub">- Web Developer Junior -</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.background{

.bg {
  animation:slide 6s ease-in-out infinite alternate;
  background-image: linear-gradient(-60deg, #231F20 50%, #BB4430 50%);
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

.swiper{
  width: 200px;
  min-height: 100px;
}

.swiper-slide {
  background-color: black;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  font-weight: bold;
  color: #fff;
  border-radius: 10px;
  .swipe_arrow{
    font-size: 0.5em;
  }
}
.swiper-slide:nth-child(1n) {
  background-color: darken(#e44c26, 10%);
  border: 5px solid #e44d26;
}

.swiper-slide:nth-child(2n) {
  background-color: darken(#2449d8, 10%);
  border: 5px solid #2449d8;
}

.swiper-slide:nth-child(3n) {
  background-color: darken(#cbb132, 10%);
  border: 5px solid #cbb132;
}

.swiper-slide:nth-child(4n) {
  background-color: darken(#7911ee, 10%);
  border: 5px solid #7911ee;
}

.swiper-slide:nth-child(5n) {
  background-color: darken(#3eaf7c, 10%);
  border: 5px solid #3eaf7c;
}

.swiper-slide:nth-child(6n) {
  background-color: darken(#7175aa, 10%);
  border: 5px solid #7175aa;
}

.swiper-slide:nth-child(7n) {
  background-color: darken(#e4453a, 10%);
  border: 5px solid #e4453a;
}

.background{
}

.main-container{
  display: flex;
  padding-top: 180px;
  height: calc(100vh - 130px);
  flex-direction: column;
  align-items: center;
  .image-container{
      width: 200px;
      padding-bottom: 20px;
      img{
        border-radius: 50%;
        width: 100%;
        height: 100%;
      }
    
  }
  .info-section{
    padding: 4px;
      margin-top: 70px;
      display: flex;
      flex-direction: column;
      h1{
        font-size: 3em;
        color: lightgray;
        text-shadow: 1px 1px 2px black;
      }
      .sub{
        text-shadow: 1px 1px 2px black;
        width: fit-content;
        overflow: hidden;
        white-space: nowrap;
        font-size: 1.5rem;
        margin: 0 auto;
        font-family: "Courier New";
        animation: typing 3s steps(38) 1s 1 normal both, blink 1s steps(1) infinite;
        text-align: center;
      }
  
      @keyframes typing {
        from {
          width: 0;
        }
        to {
          width: 100%;
        }
      }
      @keyframes blink {
        50% {
          border-color: transparent;
      }
    }
    }
    
}

@media screen and (max-width: 990px) {
  .main-container{
    padding-top: 20px;
  }
}

@media screen and (max-width: 768px) {
  #name{
    font-size: 2em;
    text-align: center;
  }
  #sub{
    font-size: 1em;
  }
}


</style>