<script>
  import routes from './routes'
  import TheNotFoundPage from './components/TheNotFoundPage'

  export default {
    name: 'App',
    data() {
      return {
        currentRoute: window.location.pathname
      }
    },
    computed: {
      ViewComponent() {
        return routes[this.currentRoute] || TheNotFoundPage
      }
    },
    render(createElement) {
      console.log('In render func');
      return createElement(
        'div',
        {
          'class': ['container'],
          attrs: {
            id: 'app'
          },
        },
        [createElement(this.ViewComponent)]
      )
    },
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
