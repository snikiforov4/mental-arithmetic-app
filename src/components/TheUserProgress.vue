<template>
  <div class="is-size-5 has-text-left">
    <p v-if="lastGameResult">The latest game result:
      correct: <span style="color: mediumseagreen">{{ lastGameResult.correct }}</span>
      wrong: <span style="color: indianred">{{ lastGameResult.incorrect }}</span>
    </p>
    <p v-if="accuracy">Accuracy: {{ accuracy }}%</p>
  </div>
</template>

<script>
  export default {
    name: 'TheUserProgress',
    data() {
      return {
        lastGameResult: {correct: 13, incorrect: 12},
      }
    },
    computed: {
      accuracy: function () {
        return 42
      }
    }
  };
</script>

