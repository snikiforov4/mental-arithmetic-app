<template>
  <div id="app" class="container">
    <p class="title is-1 has-text-left">Hello!</p>

  </div>
</template>

<script>
 import TheGame from './components/TheGame'

export default {
  name: 'App',
  components: {
    TheGame,
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
