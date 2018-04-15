<template>
  <div id="app" class="container">
    <GameControlPanel/>
    <ArithmeticExpression/>
    <Calculator/>
  </div>
</template>

<script>
import GameControlPanel from './components/GameControlPanel'
import Calculator from './components/Calculator'
import ArithmeticExpression from './components/ArithmeticExpression'

export default {
  name: 'App',
  components: {
    GameControlPanel,
    ArithmeticExpression,
    Calculator,
  }
}
</script>

<style>
#app {
  font-family: "Open Sans", "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
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
