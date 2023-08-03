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
        <form class="formContainer" @submit.prevent="sendEmail">
          <h1>Keep in touch!</h1>
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
    </div>
  </div>
</template>

<style lang="scss" scoped>

.containerForm{
  display: flex;
  flex-direction: column;
}

.form-section{
  display: flex;
  justify-content: center;
  padding-top: 70px;
}

.formContainer{
  display: flex;
  flex-direction: column;
  background-color: #231F20;
  width: 500px;
  padding: 20px;
  border-radius: 15px;
  gap: 20px;
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


</style>