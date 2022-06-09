<template>
  <div id="app">
    <demo-circle />
  </div>
</template>

<script>
import DemoCircle from './components/DemoCircle.vue'

export default {
  name: 'App',
  components: {
    DemoCircle
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
