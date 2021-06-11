<template>
  <div id="app">
    <age-solver-n :user-age="age"/>
    <label>
      Введіть вік користувача
      <input type="number" v-model="age">
    </label>
  </div>
</template>

<script>

import AgeSolverN from './components/AgeSolverN.vue'

export default {
  name: 'App',
  components: {
  
    AgeSolverN

  },
  data() {
    return {
      age: 21
    }
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
