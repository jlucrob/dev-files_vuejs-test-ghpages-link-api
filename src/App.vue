<template>
  <div id="app">
    <img src="./assets/logo.png">
    <ShowData/>
  </div>
</template>

<script>
import ShowData from './components/ShowData'

export default {
  name: 'App',
  components: {
    ShowData
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
