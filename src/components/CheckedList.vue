<template>
  <div>
    <template v-for="value in values">
      <label>
        <input type="checkbox" :value="value" v-model="chosenOperations">
        {{ value }}
      </label>
      <br>
    </template>
  </div>
</template>

<script>
  export default {
    name: 'CheckedList',
    props: {
      values: {
        type: Array,
        required: true,
      }
    },
    data() {
      return {
        chosenOperations: [],
      }
    }
  }
</script>
