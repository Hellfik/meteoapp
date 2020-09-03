<template>
  <div id="app">
    <meteo></meteo>
   
  </div>
</template>

<script>
import Meteo from './components/Meteo'

export default {
  name: 'App',
  components: {
    'meteo': Meteo
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
</style>
