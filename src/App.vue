<template>
  <div id="app">
    
    <AppHeader/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AppHeader from './components/Header.vue' // Asegúrate de que el nombre del archivo y la ruta sean correctos

export default {
  name: 'App',
  components: {
    AppHeader ,
    HelloWorld,

  }
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
