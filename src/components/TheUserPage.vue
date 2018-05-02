<template>
    <h2 class="title is-2 has-text-left">Hello!</h2>
    <UserProgress/>
    <GameSettings/>
    <a class="button is-primary is-outlined is-large is-capitalized is-pulled-right">Play</a>
</template>
<script>
  import GameSettings from './GameSettings'
  import UserProgress from './UserProgress'

  export default {
    name: 'TheUserPage',
    components: {GameSettings, UserProgress}
  }
</script>
