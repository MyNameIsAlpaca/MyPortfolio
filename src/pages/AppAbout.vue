<script>

export default {
  name: "AppAbout",
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
    <div class="container-lg">
      <div class="main-container">
        <div class="change-text">
          <h4 class="wordCarousel">
              <span>I am a</span>
              <div>
                  <ul class="flip3">
                    <li style="color:green; margin-left: -25px;">Web Developer</li>
                    <li style="color:red; margin-left: -25px;">Gamer</li>
                    <li style="color:powderblue; margin-left: -25px;">IT nerd</li>
                  </ul>
              </div>
          </h4>
        </div>
        <div class="info">
          <div class="title-container">
            <h1>
              <span>Who&nbsp;</span>
              <span>Is&nbsp;</span>
              <span>Gabriele</span>
              <span>?</span>
            </h1>
          </div>
          <div class="desc">
            <span>Nato il 3 maggio 1998 nella provincia di Sondrio ho sempre avuto una passione innata per la tecnologia, in particolare per l'informatica. 
            </span>
            <span>
              Ho sempre tenuto questa mia passione come un semplice hobby da coltivare e migliorare nel tempo libero ma il mio sogno è quello di portare questa mia passione in un ambito lavorativo dove poter crescere e migliorare giorno dopo giorno.
            </span>
            <span>Ciò che mi affascina maggiormente della programmazione è il suo carattere dinamico e la sua costante evoluzione, che ti stimola a migliorare sempre di più e ti permette di creare dal nulla progetti sempre più grandi.</span>
            <span>Uno dei tratti distintivi della mia personalità che preferisco è la <strong>curiosità</strong>, questa continua sete di conoscenza mi spinge ogni giorno a domandarmi cosa c'è dietro ai programmi e siti web che utilizziamo tutti i giorni, quale lavoro è stato fatto per creare e migliorare sempre di più un determinato prodotto.</span>
            <span class="mb-4">Sperando un giorno di poter prendere anche io parte ad un grande progetto che lascerà il segno.</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.background{
  background-color: black;
  width: 100%;
  height: 100vh;
  .main-container{
    padding-top: 100px;
    height: 100vh;
    overflow: auto;
    .desc{
      padding-top: 20px;
      text-align: center;
      display: flex;
      flex-direction: column;
      gap: 20px;
      font-size: 1.5em;
      span:nth-child(1){
        opacity: 0;
        animation: fade-in 0.8s 1s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
      span:nth-child(2){
        opacity: 0;
        animation: fade-in 0.8s 2s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
      span:nth-child(3){
        opacity: 0;
        animation: fade-in 0.8s 3s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
      span:nth-child(4){
        opacity: 0;
        animation: fade-in 0.8s 4s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
      span:last-child{
        opacity: 0;
        animation: fade-in 0.8s 5s forwards cubic-bezier(0.11, 0, 0.5, 0);
        font-style: italic;
      }
      @keyframes fade-in {
        100% {
          opacity: 1;
          filter: blur(0);
        }
      }
    }


    .title-container{
      h1 {
        transform: scale(0.94);
        animation: scale 3s forwards cubic-bezier(0.5, 1, 0.89, 1);
        text-align: center;
      }

      @keyframes scale {
        100% {
          transform: scale(1);
        }
      }
  
      span {
        display: inline-block;
        opacity: 0;
        filter: blur(4px);
      }
  
      span:nth-child(1) {
        animation: fade-in 0.8s 0.1s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
  
      span:nth-child(2) {
        animation: fade-in 0.8s 0.2s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
  
      span:nth-child(3) {
        animation: fade-in 0.8s 0.3s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }
  
      span:nth-child(4) {
        animation: fade-in 0.8s 0.4s forwards cubic-bezier(0.11, 0, 0.5, 0);
      }

  
      @keyframes fade-in {
        100% {
          opacity: 1;
          filter: blur(0);
        }
      }
    }
    .change-text{
      .wordCarousel {
        font-size: 1.5em;
        font-weight: 100;
        color: #eee;
        display: flex;
        div {
            overflow: hidden;
            position: relative;
            height: 65px;
            margin-right: -10px;
            padding-top: 10px;
            margin-top: -10px;
            li {
                font-family: Serif;
                color: #eee;
                font-weight: 700;
                padding: 0 10px;
                height: 45px;
                margin-bottom: 45px;
                display: block;
            }
        }
        .flip3 { animation: flip3 8s cubic-bezier(0.23, 1, 0.32, 1.2) infinite; }
    }

    @keyframes flip2 {
        0% { margin-top: -180px; }
        5% { margin-top: -90px;  }
        50% { margin-top: -90px; }
        55% { margin-top: 0px; }
        99.99% { margin-top: 0px; }
        100% { margin-top: -180px; }
    }

    @keyframes flip3 {
        0% { margin-top: -270px; }
        5% { margin-top: -180px; }
        33% { margin-top: -180px; }
        38% { margin-top: -90px; }
        66% { margin-top: -90px; }
        71% { margin-top: 0px; }
        99.99% { margin-top: 0px; }
        100% { margin-top: -270px; }
    }

    @keyframes flip4 {
        0% { margin-top: -360px; }
        5% { margin-top: -270px; }
        25% { margin-top: -270px; }
        30% { margin-top: -180px; }
        50% { margin-top: -180px; }
        55% { margin-top: -90px; }
        75% { margin-top: -90px; }
        80% { margin-top: 0px; }
        99.99% { margin-top: 0px; }
        100% { margin-top: -360px; }
    }

    @keyframes flip5 {
        0% { margin-top: -450px; }
        5% { margin-top: -360px; }
        20% { margin-top: -360px; }
        25% { margin-top: -270px; }
        40% { margin-top: -270px; }
        45% { margin-top: -180px; }
        60% { margin-top: -180px; }
        65% { margin-top: -90px; }
        80% { margin-top: -90px; }
        85% { margin-top: 0px; }
        99.99% { margin-top: 0px; }
        100% { margin-top: -450px; }
    }
    }
  }
}
@media screen and (max-width: 992px) {
  .background .main-container {
    .desc{
      margin: auto;
      max-width: 80%;
      font-size: 1em;
      span{
    }
    }
  }
}

</style>