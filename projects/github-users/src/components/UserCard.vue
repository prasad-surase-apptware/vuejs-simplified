<script setup>
import { defineProps } from 'vue'
const { profilePic, userName, profileLink } = defineProps(['profilePic', 'userName', 'profileLink'])
</script>

<template>
  <div class="card">
    <img :src="profilePic" width="100px" alt="user profile" />
    <h1>{{ userName }}</h1>
    <a :href="profileLink" class="btn">View Profile!</a>
  </div>
</template>

<style>
.card {
  width: 150px;
  background: white;
  border-radius: 10px;
  padding: 2rem;

  display: flex;
  flex-direction: column;
  align-items: center;
}

.card > img {
  border-radius: 50%;
}

.btn {
  background-color: black;
  color: white;
  cursor: pointer;
  padding: 1rem;
  outline: none;
  border: 1px solid black;
  border-radius: 7px;
  text-decoration: none;
}
</style>
