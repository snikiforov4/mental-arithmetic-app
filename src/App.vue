<template>
  <div id="app">
    <HelloWorld/>
  </div>
</template>

<script>
import GameControlPanel from './components/GameControlPanel'

export default {
  name: 'App',
  components: {
    GameControlPanel
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
  margin-top: 2em;
}
</style>
