<template>
  <div id="app" class="container">
    <the-user-page></the-user-page>
  </div>
</template>

<script>
  import TheUserPage from "./components/TheUserPage";
  import TheGame from './components/TheGame'

  export default {
  name: 'App',
  components: {
    TheUserPage,
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
