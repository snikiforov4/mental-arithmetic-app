<template>
    <div>
      <h2 class="title is-2 has-text-left">Hello!</h2>
      <the-user-progress></the-user-progress>
      <the-user-settings></the-user-settings>
      <a class="button is-primary is-outlined is-large is-capitalized is-pulled-right">Play</a>
    </div>
</template>
<script>
  import TheUserProgress from './TheUserProgress'
  import TheUserSettings from './TheUserSettings'

  export default {
    name: 'TheUserPage',
    components: {TheUserProgress, TheUserSettings}
  }
</script>
