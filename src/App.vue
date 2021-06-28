<template>
  <div id="app">
    <!--<example-login :userDataArray="userDataArray"/> 
    <br>
    <button @click="go">Go</button>
    <WordCard v-if="randomObject"
    :imageSrc = "randomObject.src"
    :enTranslate = "randomObject.enTranslate"
    :uaTranslate = "randomObject.uaTranslate"
    />
   <avia-tickets/> -->
   <ticket-form/>


  </div>
</template>
<script>
//import AviaTickets from './components/AviaTickets.vue';
//import ExampleLogin from './components/ExampleLogin.vue'
//import WordCard from './components/WordCard.vue'
import TicketForm from './components/TicketForm.vue'




export default {
  name: 'App',
  components: {
    //AviaTickets
    //ExampleLogin,
    //WordCard
    TicketForm
  },
  data() {
    return {
      userDataArray: [
      {
        login: "Ivan", 
        pass: 111
      },
      {
      login: "Petro", 
      pass: 222
      },
      {
      login: "Roma", 
      pass: 333
      },
      {
      login: "Stas", 
      pass: 444
      }, 
    ],
    translationList: [
      {
          id: 1,
          src:
            "https://www.ikea.com/cz/en/images/products/ekedalen-extendable-table-dark-brown__0736963_pe740827_s5.jpg",
          enTranslate: "table",
          uaTranslate: "стіл",
        },
        {
          id: 2,
          src:
            "https://penworld.sirv.com/media/catalog/product/1/9/1953191_1.jpg?scale.option=ignore&canvas.width=1600&canvas.height=1600&w=1600&h=933&canvas.opacity=0",
          enTranslate: "pen",
          uaTranslate: "ручка",
        },
        {
          id: 3,
          src:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Apple_logo_black.svg/1200px-Apple_logo_black.svg.png",
          enTranslate: "apple",
          uaTranslate: "яблуко",
        }
     ],
      nameRandom : null,
      randomObject : null,
    };
  },
  methods: {
    go() {
      this.nameRandom = Math.floor(Math.random()*this.translationList.length)
      this.randomObject = this.translationList[this.nameRandom]
    }
  },
}
</script>










<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
