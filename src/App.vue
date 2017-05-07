<template>
  <div id="app">
    <data-tables data='data from server'></data-tables>
  </div>
</template>

<script>
import Hello from './components/Hello'
import DataTables from './components/DataTables'

export default {
  name: 'app',
  components: {
    Hello,DataTables
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
