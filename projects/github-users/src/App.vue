<script setup>
import { onMounted, ref } from 'vue'
import UserCard from './components/UserCard.vue'

const users = ref([])

const fetchUsers = () => {
  fetch('https://api.github.com/users')
    .then((res) => res.json())
    .then((data) => {
      console.log('data', data)
      users.value = data
    })
}

onMounted(() => {
  fetchUsers()
})
</script>

<template>
  <h1 style="color: white; text-align: center">Github Users!</h1>

  <div class="usersContainer">
    <UserCard
      v-for="user in users"
      v-bind:profilePic="user.avatar_url"
      :userName="user.login"
      :profileLink="user.html_url"
    />
  </div>
</template>

<style>
body {
  background: linear-gradient(
    90deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(9, 9, 121, 1) 35%,
    rgba(0, 212, 255, 1) 100%
  );
}

.usersContainer {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}
</style>
