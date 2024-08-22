<script setup>
import { useCounter } from "../composables/useCounter";

const { count, increment, decrement } = useCounter();
</script>

<template>
  <div>
    <p>Count: {{ count }}</p>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
  </div>
</template>
