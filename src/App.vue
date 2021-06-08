<template>
  <div id="app">
    <age-solver :user-age="64"/>
  </div>
</template>

<script>
import AgeSolver from './components/AgeSolver.vue'

export default {
  name: 'App',
  components: {
    AgeSolver
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
