<template>
  <div>
    <the-game-control-panel></the-game-control-panel>
    <the-game-arithmetic-expression></the-game-arithmetic-expression>
    <the-game-key-pad></the-game-key-pad>
  </div>
</template>

<script>
  import TheGameControlPanel from './TheGameControlPanel'
  import TheGameArithmeticExpression from './TheGameArithmeticExpression'
  import TheGameKeyPad from './TheGameKeyPad'

  export default {
    name: "TheGame",
    components: {
      TheGameControlPanel,
      TheGameArithmeticExpression,
      TheGameKeyPad,
    }
  }
</script>

