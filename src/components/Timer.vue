<template>
    <span class="title is-1 is-pulled-right">{{ formattedLeftTime }}</span>
</template>

<script>
  import moment from 'moment';
  import 'moment-duration-format';

  export default {
    name: 'Timer',
    props: {
      'initialLeftTime': {
        type: [Number, String],
        required: true,
        default: 10 * 60,
      },
    },
    data() {
      return {
        endTime: null,
        leftTime: Number(this.initialLeftTime),
        timerId: null,
      }
    },
    mounted() {
      this.endTime = moment().add(this.initialLeftTime, 'seconds');
      this.timerId = window.setInterval(() => {
        this.leftTime = this.endTime.diff(moment(), 'seconds');
      }, 1000);
    },
    beforeDestroy() {
      if (this.timerId) window.clearInterval(this.timerId);
    },
    computed: {
      formattedLeftTime: function () {
        return moment.duration(this.leftTime, "seconds").format('mm:ss')
      }
    }
  }
</script>
