<script setup>
import { reactive, ref } from "vue";

const state = reactive({
  counter: 0,
  counter2: 100,
});
// const state = ref({
//   counter: 0,
//   counter2: 100,
// });

let counter3 = ref(10);
</script>

<template>
  <h1>Reactivity in Vue!</h1>

  <ol>
    <li>reactive()</li>
    <li>ref()</li>
  </ol>

  <hr />

  <h2>Reactivity for objects/arrays:</h2>

  <h3>Counter1: {{ state.counter }}</h3>
  <h3>Counter2: {{ state.counter2 }}</h3>

  <button class="btn" @click="state.counter++">Increment!</button>
  <button class="btn" @click="state.counter2--">Decrement!</button>

  <hr />

  <h2>Reactivity for simple values:</h2>

  <h3>Counter3: {{ counter3 }}</h3>

  <button class="btn" @click="counter3++">Mutiply by 2</button>
</template>
