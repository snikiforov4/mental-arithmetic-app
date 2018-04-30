<template>
    <div>
      <label>
        <input type="range" :min="min" :max="max" class="slider" v-model="value">
        {{ label}} {{ value }}
      </label>
    </div>
</template>
<script>
  export default {
    name: 'Slider',
    props: {
      min: {
        type: [String, Number],
        required: true,
      },
      max: {
        type: [String, Number],
        required: true,
      },
      label: {
        type: String,
      },
    },
    data() {
      return {
        value: this.min,
      }
    },
  }
</script>
<style scoped>

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
