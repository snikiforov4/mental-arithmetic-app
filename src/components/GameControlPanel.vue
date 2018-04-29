<template>
  <div class="columns">
    <div class="column is-two-thirds">
      <a class="button is-danger is-outlined is-large is-capitalized is-pulled-left">Cancel</a>
    </div>
    <div class="column is-one-third">
      <span class="title is-1 is-pulled-right">{{ formattedLeftTime }}</span>
    </div>
  </div>
</template>

<script>
  import moment from 'moment';
  import 'moment-duration-format';
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
        leftTime: Number(this.gameDuration),
      }
    },
    mounted() {
      this.gameEndTime = moment().add(this.gameDuration, 'seconds');
      window.setInterval(() => {
        this.leftTime = this.gameEndTime.diff(moment(), 'seconds');
      }, 1000);
    },
    computed: {
      formattedLeftTime: function () {
        return moment.duration(this.leftTime, "seconds").format('mm:ss')
      }
    }
  }
</script>
