<script setup>
import { ref, computed } from "vue";

let firstName = ref("Prasad");
let lastName = ref("Surase");

let fullName = computed(() => firstName.value + " " + lastName.value);
</script>

<template>
  <h1>Computed Properties!</h1>

  <input type="text" placeholder="first name" v-model="firstName" />
  <br /><br />
  <input type="text" placeholder="last name" v-model="lastName" />
  <h4>First Name Is: {{ firstName }}</h4>
  <h4>Last Name Is: {{ lastName }}</h4>
  <h4>Full Name Is: {{ fullName }}</h4>
</template>
