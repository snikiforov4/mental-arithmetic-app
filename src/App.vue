<template>
  <div id="app" class="container">
    <h2 class="title is-2 has-text-left">Hello!</h2>
    <UserProgress/>
    <GameSettings/>
    <a class="button is-primary is-outlined is-large is-capitalized is-pulled-right">Play</a>
  </div>
</template>

<script>
 import TheGame from './components/TheGame'
import UserProgress from './components/UserProgress'
import GameSettings from './components/GameSettings'

export default {
  name: 'App',
  components: {
    TheGame,
    UserProgress,
    GameSettings,
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
