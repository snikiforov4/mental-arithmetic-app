<template>
  <div class="settings content is-size-5 has-text-left">
    <h2 class="title is-2">Settings</h2>
    <Slider v-bind="duration"/>
    <Slider v-bind="difficulty"/>
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
        duration: {
          min: 1,
          max: 15,
          default: 10,
          label: 'Game duration',
        },
        difficulty: {
          min: 1,
          max: 3,
          label: 'Game difficulty',
        },
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
