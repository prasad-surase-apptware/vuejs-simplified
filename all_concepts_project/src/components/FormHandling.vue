<script setup>
const handleFormData = () => {
  console.log("Form Submitted!");
  //   add your logic
};
</script>

<template>
  <form @submit.prevent="handleFormData">
    <input type="email" placeholder="Enter your email" />
    <input type="password" placeholder="Enter your password" />
    <input type="submit" value="Login" />
  </form>
</template>
