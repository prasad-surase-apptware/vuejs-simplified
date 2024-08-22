<script setup></script>

<template>
  <h1>CSS Modules!</h1>

  <!-- <input
    type="text"
    placeholder="Enter something"
    :class="$style['input-field']"
  />
  <button :class="$style.btn">Register</button> -->
  <input
    type="text"
    placeholder="Enter something"
    :class="ashish['input-field']"
  />

  <button :class="ashish.btn">Register</button>
</template>

<!-- local styling/ component specific -->
<!-- <style module> -->
<style module="ashish">
.btn {
  background-color: black;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 7px;
  border: 1px solid black;
  cursor: pointer;
}
.input-field {
  padding: 0.5rem;
}
</style>
