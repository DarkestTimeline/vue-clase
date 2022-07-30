<template>
  <img alt="Vue logo" src="./assets/sis_logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <test/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// Importar modulo
import Test from './components/Test.vue'

export default {
  name: 'App',
  components: {
    //HelloWorld,
    Test
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
img{
  width: 250px;
}
</style>
