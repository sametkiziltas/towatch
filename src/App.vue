<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <WatchList msg="İşte izleme listen burada"/>
  </div>
</template>

<script>
import WatchList from './components/WatchList.vue'

export default {
  name: 'app',
  components: {
    WatchList
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
