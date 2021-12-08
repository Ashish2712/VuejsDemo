<template>
  <div id="app">
    <Names/>
  </div>
</template>
<script>
import Names from './components/Names.vue'
export default {
  name: 'app',
  components: {
    Names
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