<template>
  <div>
    <the-game-control-panel game-duration='900'></the-game-control-panel>
    <ArithmeticExpression/>
    <Calculator/>
  </div>
</template>

<script>
  import TheGameControlPanel from './TheGameControlPanel'
  import Calculator from './Calculator'
  import ArithmeticExpression from './ArithmeticExpression'

  export default {
    name: "TheGame",
    components: {
      TheGameControlPanel,
      ArithmeticExpression,
      Calculator,
    }
  }
</script>

