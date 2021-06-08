<template>
  <div id="app">
    <age-solver :user-age="age"/>
    <age-solver-n :user-age="age"/>
    <label>
      Введіть вік користувача
      <input type="number" v-model="age">
    </label>
  </div>
</template>

<script>
import AgeSolver from './components/AgeSolver.vue'
import AgeSolverN from './components/AgeSolverN.vue'

export default {
  name: 'App',
  components: {
    AgeSolver,
    AgeSolverN,

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
