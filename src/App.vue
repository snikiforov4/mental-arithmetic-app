<template>
  <div id="app" class="container">
    <GameControlPanel/>
    <Calculator/>
  </div>
</template>

<script>
import GameControlPanel from './components/GameControlPanel'
import Calculator from './components/Calculator'

export default {
  name: 'App',
  components: {
    GameControlPanel,
    Calculator
  }
}
</script>

<style>
#app {
  font-family: "Raleway", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 2em;
}
.container {
  max-width: 700px;
  width: 700px;
}
</style>
