<script setup>
let value = false;

// Option 1
// const vFocus = {
//   mounted(el, binding) {
//     console.log(el);
//   },
// };

// Option 2
const vFocus = (el) => el.focus();

// const vColor = (el, binding) => (el.style.color = binding.value || "hotpink");
const vColor = (el, binding) =>
  (el.style.color = binding.value.color || "hotpink");
</script>

<template>
  <h1>Custom Directives</h1>

  <h2>v-focus</h2>
  <input type="text" placeholder="vFocus demo!" v-focus />

  <hr />
  <h2>v-color</h2>
  <h3 v-color="'green'">This is the demo of v-color custom directive!</h3>
  <h3 v-color="{ color: 'blue', text: 'hello!' }">
    This is the demo of v-color custom directive!
  </h3>
</template>
