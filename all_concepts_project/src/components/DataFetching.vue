<script setup>
const fetchTodos = () => {
  fetch("https://jsonplaceholder.typicode.com/todos")
    .then((res) => res.json())
    .then((data) => console.log("data", data));
};
</script>

<template>
  <h1>Data Fetching - Using Fetch API</h1>
  <button class="btn" @click="fetchTodos">Fetch Data!</button>
</template>
