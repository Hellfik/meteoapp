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

body{
  background: #BBD2C5;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #536976, #BBD2C5);  /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, #536976, #BBD2C5); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}
</style>
