<template>
  <div id="app">
    <demo-multi-circle />
  </div>
</template>

<script>
import DemoMultiCircle from './components/DemoMultiCircle.vue'

export default {
  name: 'App',
  components: {
    DemoMultiCircle
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
