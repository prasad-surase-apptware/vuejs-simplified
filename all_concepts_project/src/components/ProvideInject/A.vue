<script setup>
import B from "./B.vue";

import { provide } from "vue";

provide("theme", "dark");

</script>

<template>
  <h1>Parent Component - Project & Inject</h1>
  <h1>A</h1>
  <B />
</template>
