<template>
  <div id="app">

    <Cep />
  </div>
</template>

<script>
import Cep from './components/Cep.vue'

export default {
  name: 'app',
  components: {
    Cep
  },
  data: function () {
    return {
      a: 3,
      b: 5
    }
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
  margin-top: 60px;
}
</style>
