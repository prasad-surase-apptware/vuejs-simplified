<script setup></script>

<template>
  <h1>Styling In Vue JS!</h1>

  <button class="btn">Register</button>
</template>

<!-- local styling/ component specific -->
<style scoped>
.btn {
  background-color: green;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 7px;
  border: 1px solid greenyellow;
  cursor: pointer;
}
</style>

<!-- global styling -->
<style>
.btn {
  background-color: black;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 7px;
  border: 1px solid black;
  cursor: pointer;
}
</style>

<!-- combined style = local + glbal style blocks -->
