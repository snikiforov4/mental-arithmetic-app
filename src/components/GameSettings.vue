<template>
  <div class="settings content is-size-5 has-text-left">
    <h2 class="title is-2">Settings</h2>
    <input type="range" min="1" max="15" class="slider" v-model="duration" id="duration">
    <label for="duration">Game duration {{ duration }}</label>
    <input type="range" min="1" max="3" class="slider" v-model="difficulty" id="difficulty">
    <label for="difficulty">Game difficulty {{ difficulty }}</label>
    <CheckedList :values="operations"/>
  </div>
</template>

<script>
  import CheckedList from "./CheckedList";

  export default {
    name: 'GameSettings',
    components: {CheckedList},
    data() {
      return {
        duration: 7,
        difficulty: 2,
        operations: ['addition', 'subtraction', 'multiplication', 'division'],
      }
    },
  };
</script>

<style scoped>
  .settings {
    margin: 2em 0;
  }

  .slider {
    -webkit-appearance: none;
    width: 100%;
    height: 10px;
    border-radius: 5px;
    background: #d3d3d3;
    outline: none;
    opacity: 0.7;
    -webkit-transition: .2s;
    transition: opacity .2s;
  }

  .slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    width: 25px;
    height: 25px;
    border-radius: 50%;
    background: #4CAF50;
    cursor: pointer;
  }

  .slider::-moz-range-thumb {
    width: 25px;
    height: 25px;
    border-radius: 50%;
    background: #4CAF50;
    cursor: pointer;
  }
</style>
