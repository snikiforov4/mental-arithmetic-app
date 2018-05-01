<template>
  <div class="columns">
    <div class="column is-half">
      <a class="button is-danger is-outlined is-large is-capitalized is-pulled-left">Cancel</a>
    </div>
    <div class="column is-half">
      <timer :initial-left-time="gameDuration"></timer>
    </div>
  </div>
</template>

<script>
  import Timer from "./Timer";

  export default {
    name: 'TheGameControlPanel',
    components: {Timer},
    data() {
      return {
        gameDuration: 10 * 60,
      }
    },
  }
</script>
