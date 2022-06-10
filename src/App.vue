<template>
  <div id="app">
    <demo-circle-line />
  </div>
</template>

<script>
import DemoCircleLine from './components/DemoCircleLine.vue'

export default {
  name: 'App',
  components: {
    DemoCircleLine
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
