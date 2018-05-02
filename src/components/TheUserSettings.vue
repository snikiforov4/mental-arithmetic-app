<template>
  <div class="settings content is-size-5 has-text-left">
    <h2 class="title is-2">Settings</h2>
    <slider v-bind="duration"></slider>
    <slider v-bind="difficulty"></slider>
    <checked-list :values="operations"></checked-list>
  </div>
</template>

<script>
  import Slider from "./Slider";
  import CheckedList from "./CheckedList";

  export default {
    name: 'TheUserSettings',
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
