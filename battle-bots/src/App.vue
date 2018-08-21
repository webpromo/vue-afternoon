<template>
  <div id="app">
    <header>
      <div><button>CREATE</button></div>
      <div><span style="font-size:14pt;">Battle Bots</span></div>
      <div><button>COLLECTION</button></div>
    </header>

    <section class="formBox">
      <div class="formElement">Bot Name* <input /></div>
      <div class="formElement">Attack Value* <input /></div>
      <div class="formElement">Health Value* <input /></div>
      <div class="formElement"><button>SUBMIT</button> &nbsp; <button>CLEAR</button></div>

    
      
    </section>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
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
