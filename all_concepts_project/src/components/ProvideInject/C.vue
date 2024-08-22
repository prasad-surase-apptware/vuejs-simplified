<script setup>
import { inject } from "vue";

const theme = inject("theme")
</script>

<template>
  <h1>C - {{theme}}</h1>
</template>
