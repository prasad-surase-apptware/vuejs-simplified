<script setup>
function sayHello() {
  alert("Hello, Just checking if you're having a good day!");
}

let counter = 0;
</script>

<template>
  <h1>Event Handling!</h1>

  <button class="btn" v-on:click="sayHello()">Say Hello!</button>
  <button class="btn" @click="sayHello()">Say Hello!</button>
  <button class="btn" @click="sayHello">Say Hello!</button>

  <hr />

  <h3>Counter {{ counter }}</h3>
  <button class="btn" @click="counter++">+</button>
</template>
