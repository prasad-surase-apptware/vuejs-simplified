<script setup>
let isAdmin = true;
let isSuperAdmin = false;

let isHungry = true;

// for v-for demonstration
const items = ["Sugar", "Peanuts", "Soya", "Oil", "Maida"];
</script>

<template>
  <h1>Conditional Rendering!</h1>

  <ol>
    <li>v-if</li>
    <li>v-else-if</li>
    <li>v-else</li>
    <li>v-show</li>
    <li>v-for</li>
  </ol>

  <hr />

  <div>
    <h3>User Type:</h3>
    <p v-if="isSuperAdmin">Super Admin</p>
    <p v-else-if="!isSuperAdmin && isAdmin">Admin</p>
    <p v-else>User</p>
  </div>

  <hr />

  <div>
    <h4>v-if:</h4>
    <p v-show="isHungry">Time to make some breakfast!</p>
    <p v-show="!isHungry">Nah, we can just have a coffee!</p>
  </div>

  <hr />

  <div>
    <h1>v-for [eg. Grocery List]</h1>
    <!-- <ol>
      <li>{{ items[0] }}</li>
      <li>{{ items[1] }}</li>
      <li>{{ items[2] }}</li>
    </ol> -->

    <p class="pill" v-for="(item, i) of items" :key="item">
      {{ i + 1 + ". " + item }}
    </p>
  </div>

  <!-- <div v-for="project of projectList" :key="project.id">
    <div v-for="task of project.tasksList">
      <p>{{ task.id }}</p>
      <p>{{ task.name }}</p>
    </div>
  </div> -->
</template>

<style scoped>
.pill {
  background-color: purple;
  color: white;
  border-radius: 10px;
  display: inline-block;
  padding: 5px;
  margin: 5px;
}
</style>
