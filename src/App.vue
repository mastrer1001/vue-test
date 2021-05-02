<template>
  <div id="app">
    <img alt="Spagetti" src="./assets/carbonara.jpg">
    <HelloWorld message="Spagetti Carbonara" intro="Carbonara ist ein Nudelgericht aus Pasta mit Guanciale, Ei, Pfeffer und Käse aus der italienischen Region Latium. Es gehört zu den Klassikern der italienischen Küche."
                button="btn1"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
