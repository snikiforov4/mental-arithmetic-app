<template>
  <div class="columns">
    <div class="column is-two-thirds">
      <a class="button is-danger is-outlined is-large is-capitalized is-pulled-left">
        Cancel
      </a>
    </div>
    <div class="column is-one-third">
      <span class="title is-1 is-pulled-right">{{ leftTime }}</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'GameControlPanel',
    props: {
      'gameDuration': {
        type: [Number, String],
        default: 10 * 60,
      },
    },
    data() {
      return {
        gameEndTime: null,
        leftTime: null,
      }
    },
    created() {
      this.leftTime = Math.trunc(Number(this.gameDuration));
    },
    mounted() {
      this.gameEndTime = Math.trunc((new Date()).getTime() / 1000) + Number(this.gameDuration);
      window.setInterval(() => {
        this.leftTime = this.gameEndTime - Math.trunc((new Date()).getTime() / 1000);
      }, 1000);
    },
  }
</script>
