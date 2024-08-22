<script setup>
const imgUrl =
  "https://play-lh.googleusercontent.com/IkcyuPcrQlDsv62dwGqteL_0K_Rt2BUTXfV3_vR4VmAGo-WSCfT2FgHdCBUsMw3TPGU";
</script>

<template>
  <button class="btn">Styling test!</button>

  <h1>1. Attribute Binding! (bind some static value)</h1>
  <img
    src="https://play-lh.googleusercontent.com/IkcyuPcrQlDsv62dwGqteL_0K_Rt2BUTXfV3_vR4VmAGo-WSCfT2FgHdCBUsMw3TPGU"
    alt="there was no img!"
  />
  <input type="text" placeholder="Enter something..!" disabled />

  <hr />
  <h1>2. Dynamic Binding! (bind dynamic value)</h1>

  <img v-bind:src="imgUrl" alt="there was no img!" />

  <img :src="imgUrl" alt="there was no img!" />
</template>
