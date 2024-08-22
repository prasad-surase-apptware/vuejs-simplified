<script setup>
import { defineProps } from "vue";

const props = defineProps(["userName", "email"]);
console.log(props);
</script>

<template>
  <h1>Props</h1>
  <h1>User Name : {{ props.userName }}</h1>
  <h1>User Email : {{ props.email }}</h1>
</template>
