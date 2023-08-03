<script>
export default {
  name: "AppContact",
  data() {
    return {
      name: '',
      email: '',
      message: ''
    };
  },
  created() {
  
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_8zmyy9m', 'template_tr96drn', e.target,
        'M36i5HiTnxK88OXeD', {
          name: this.name,
          email: this.email,
          message: this.message
        })

      } catch(error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
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
    <div class="container form-section">
      <div class="containerForm">
        <div class="left-side">
          <form class="formContainer" @submit.prevent="sendEmail">
            <h2>Get in Touch!</h2>
            <label>Nome</label>
            <input class="info"
              type="text"
              v-model="name"
              name="name"
              placeholder="Inserisci il tuo nome"
            >
            <label>Email</label>
            <input class="info"
              type="email"
              v-model="email"
              name="email"
              placeholder="Inserisci la tua email"
            >
            <label>Messaggio</label>
            <textarea
            class="message"
              name="message"
              v-model="message"
              cols="30" rows="5"
              placeholder="  Inserisci un messaggio"
            ></textarea>
    
            <input class="btn btn-secondary" type="submit" value="Send">
          </form>
        </div>
        <div class="right-side">
          <h1>Contatti:</h1>
          <div class="info-contact-container">
            <div class="info-contact">
              <i class="fa-solid fa-envelope"></i><span>saragosagabriele@gmail.com</span>
            </div>
            <hr>
            <div class="info-contact">
              <i class="fa-solid fa-phone"></i><span>+39 331 830 7244</span>
            </div>
            <hr>
          </div>
          <div class="link">
            <a href="https://github.com/MyNameIsAlpaca"><i class="fa-brands fa-github"></i></a>
            <a href="https://www.linkedin.com/in/saragosa-gabriele"><i class="fa-brands fa-linkedin"></i></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.right-side{
  display: flex;
  flex-direction: column;
  gap: 20px;
  justify-content: center;
  height: 100%;
  .info-contact-container{
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
  .link{
    display: flex;
    justify-content: space-around;
    font-size: 2em;
    align-items: center;
  }
}

.info-contact{
  display: flex;
  align-items: center;
  gap: 10px;
}

.containerForm{
  display: flex;
  padding: 20px;
  background-color: #231f20a2;
  margin-top: 200px;
  border-radius: 15px;
  gap: 100px;
}

.form-section{
  display: flex;
  justify-content: center;
  
}

.formContainer{
  display: flex;
  flex-direction: column;
  gap: 20px;
  width: 500px;
  .info{

    background-color: transparent;
    color: white;
    border: 0;
    border-bottom: 1px solid white;
    border-left: 1px solid white;
  }
  .message{
    background-color: transparent;
    border: 0;
    border-bottom: 1px solid white;
    border-left: 1px solid white;
    color: white;
  }
}

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

@media screen and (max-width: 990px){
  .containerForm{
    flex-direction: column-reverse;
    margin-bottom: 50px;
    margin-top: 10px;
    gap: 30px;
  }
  
}

@media screen and (max-width: 600px){
  .formContainer{
  
  width: 100%;
  }
  .containerForm{
    width: calc(100% - 60px);
  }
}

@media screen and (max-width: 600px){
  .info-contact{
    font-size: 0.8em;
  }
}


</style>