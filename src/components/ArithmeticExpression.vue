<template>
  <div class="columns breadcrumb">
    <div class="column is-unselectable">
      <p class="is-size-2">{{ operation }}</p>
      <span class="is-size-6 is-uppercase has-text-grey-lighter">should equal to</span>
      <p class="is-size-1">{{ result }}</p>
    </div>
  </div>
</template>

<script>
  const OPERATORS = Object.freeze({ADDITION: '+', SUBTRACTION: '-', MULTIPLICATION: '*', DIVISION: '/'});

  export default {
    name: 'ArithmeticExpression',
    data() {
      return {
        operands: [11, 21, null],
        operators: [OPERATORS.ADDITION, OPERATORS.ADDITION],
        result: 42
      }
    },
    computed: {
      operation: function () {
        let res = this.operands && this.operands[0] || '';
        for (let i = 1; i < this.operands.length; i++) {
          res += this.operators[i - 1] || this.operators[0];
          res += this.operands[i] ? this.operands[i] : '__';
        }
        return res;
      }
    }
  }
</script>

