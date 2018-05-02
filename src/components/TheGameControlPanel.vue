<template>
  <div class="columns">
    <div class="column is-half">
      <a href="/" class="button is-danger is-outlined is-large is-capitalized is-pulled-left">Cancel</a>
    </div>
    <div class="column is-half">
      <timer-item :initial-left-time="gameDuration"></timer-item>
    </div>
  </div>
</template>

<script>
  import TimerItem from "./TimerItem";

  export default {
    name: 'TheGameControlPanel',
    components: {TimerItem},
    data() {
      return {
        gameDuration: 10 * 60,
      }
    },
  }
</script>
