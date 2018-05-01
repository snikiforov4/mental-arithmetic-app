<template>
  <div>
    <GameControlPanel game-duration='900'/>
    <ArithmeticExpression/>
    <Calculator/>
  </div>
</template>

<script>
  import GameControlPanel from 'GameControlPanel'
  import Calculator from 'Calculator'
  import ArithmeticExpression from 'ArithmeticExpression'

  export default {
    name: "TheGame",
    components: {
      GameControlPanel,
      ArithmeticExpression,
      Calculator,
    }
  }
</script>

