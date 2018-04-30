<template>
  <div class="settings content is-size-5 has-text-left">
    <h2 class="title is-2">Settings</h2>
    <Slider :min="durationRange.min" :max="durationRange.max" label="Game duration"/>
    <Slider :min="difficultyRange.min" :max="difficultyRange.max" label="Game difficulty"/>
    <CheckedList :values="operations"/>
  </div>
</template>

<script>
  import Slider from "./Slider";
  import CheckedList from "./CheckedList";

  export default {
    name: 'GameSettings',
    components: {Slider, CheckedList},
    data() {
      return {
        durationRange: {
          min: 1,
          max: 15,
        },
        difficultyRange: {min: 1, max: 3},
        operations: ['addition', 'subtraction', 'multiplication', 'division'],
      }
    },
  };
</script>

<style scoped>
  .settings {
    margin: 2em 0;
  }
</style>
