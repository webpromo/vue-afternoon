<template>
  <div id="app">
    <header>
      <div><button @click='toggle("form")'>CREATE</button></div>
      <div><span style="font-size:14pt;">Battle Bots</span></div>
      <div><button @click='toggle("collection")'>COLLECTION</button></div>
    </header>

      <form class='formBox' @submit.prevent='createBot'>
        <div class="formElement">Bot Name* <input 
            v-model='name' 
            type="text" 
            placeholder="enter the bot's name"></div>
        
        <div class="formElement">Attack Value* <input
            v-model='attack' 
            type="text" 
            placeholder="enter numbers"></div>

        <div class="formElement">Health Value* <input
            v-model='health' 
            type="text" 
            placeholder="enter numbers"></div>
        <div class="formElement"><button>SUBMIT</button> &nbsp; <button>CLEAR</button></div>

    </form>
    
  </div>
</template>

<script>
import Bot from './components/Bot';

export default {
  name: 'app',
  data() {
    return {
      showForm: true,
      bot: '',
      blogPost: '',
      botClub: []
    };
  },
  methods: {
    toggle(val) {
      this.showForm = val === 'form' ? true : false;
    },
    createBot() {
      let newBot = {
        name: this.name,
        attack: this.attack,
        health: this.health
      };
      this.posts.push(newPost);
      this.author = '';
      this.blogPost = '';
      this.showForm = false;
    }
  },
  components: { Bot } // {Bot: Bot}
}
</script>

<style>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    width:100%;
    height:100vh;
    background-image: linear-gradient(to bottom right, #5CDB95, #8093F1);
    margin:0px;  padding:0px;
  }
  header {
    color:white;
    width:100%;
    height:80px;
    background-color:#05386B;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
  }
  .formBox {
    padding-top:10px;
    margin:60px auto;
    width:450px;
    height:300px;
    background-color:white;
    border:1px solid #ddd;
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;

  }
</style>
