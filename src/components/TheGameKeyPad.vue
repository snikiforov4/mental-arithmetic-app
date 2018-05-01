<template>
  <div class="columns">
    <div class="column is-offset-one-fifth is-three-fifths">
      <div class="columns" v-for="rows in layout">
        <div class="column" v-for="row in rows">
          <button :class="row.type" :key="row.sign" v-if="row">{{ row.sign }}</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TheGameKeyPad',
    data() {
      return {
        layout: [
          [
            {sign: '1', type: 'digit'}, {sign: '2', type: 'digit'},
            {sign: '3', type: 'digit'}, {sign: '>', type: 'operator'},
          ],
          [
            {sign: '4', type: 'digit'}, {sign: '5', type: 'digit'},
            {sign: '6', type: 'digit'}, {sign: '<', type: 'operator'},
          ],
          [
            {sign: '7', type: 'digit'}, {sign: '8', type: 'digit'},
            {sign: '9', type: 'digit'}, null,
          ],
          [
            null, {sign: '0', type: 'digit'}, null, {sign: '=', type: 'operator'},
          ],
        ]
      }
    }
  }
</script>

<style scoped>
  button {
    width: 2em;
    height: 2em;
    outline-style: none;
    border: none;
    border-radius: 50%;
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    color: white;
    cursor: pointer;
    font-size: 2em;
    opacity: 0.8;
    transition: 0.2s;
  }

  button:hover {
    opacity: 1
  }

  .operator {
    background-color: lightsteelblue;
  }

  .digit {
    background-color: coral;
  }
</style>


