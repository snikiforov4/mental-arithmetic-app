<template>
  <div class="is-unselectable">
    <p class="is-size-2">
      <span v-for="({value, changeable}, idx) in expArgs"
            class="fixed-arg-column"
            :class="{changeable: changeable, 'editable': idx === editedArgIdx}"
            :key="idx">{{ value ? value : '   '}}</span>
    </p>
    <p class="is-size-6 is-uppercase has-text-grey-lighter">should equal to</p>
    <p class="is-size-1">{{ result }}</p>
  </div>
</template>

<script>
  export default {
    name: 'ArithmeticExpression',
    data() {
      return {
        expArgs: [
          {value: null, changeable: true},
          {value: '+', changeable: false},
          {value: 21, changeable: false},
          {value: '+', changeable: false},
          {value: null, changeable: true},
        ],
        result: 42,
        editedArgIdx: -1,
      }
    },
    created() {
      this.editedArgIdx = this.expArgs.findIndex(arg => arg.changeable);
    },
    methods: {
      editNextOperand: function () {
        const argsLen = this.expArgs.length;
        for (let i = (this.editedArgIdx + 1) % argsLen, cnt = 0; cnt < argsLen; i = (i + 1) % argsLen, cnt++) {
          if (this.expArgs[i].changeable) {
            this.editedArgIdx = i;
            return
          }
        }
      },
      editPrevOperand: function () {
        const argsLength = this.expArgs.length;
        for (let i = (argsLength + this.editedArgIdx - 1) % argsLength, cnt = 0; cnt < argsLength; i = (argsLength + i - 1) % argsLength, cnt++) {
          if (this.expArgs[i].changeable) {
            this.editedArgIdx = i;
            return
          }
        }
      },
    }
  };
</script>

<style scoped>
  .fixed-arg-column {
    white-space: pre;
    display: inline-block;
    min-width: 1rem;
    min-height: 3rem;
    padding: 0 1rem;
    border: 2px solid transparent;
  }

  .changeable {
    background-color: antiquewhite;
    border-radius: 4px;
  }

  .editable {
    border: 2px solid coral;
  }

</style>
