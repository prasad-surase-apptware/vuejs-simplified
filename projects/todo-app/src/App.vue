<script setup>
import { ref } from 'vue'
// store all tasks
const tasks = ref([])

const newTask = ref('')

// add new task
const addTask = () => {
  if (newTask.value) {
    if (tasks.value.includes(newTask.value)) {
      alert("You can't add duplicate tasks!")
    } else {
      tasks.value.push(newTask.value)
      newTask.value = ''
    }
  } else {
    alert('Please enter task first!')
  }
}

// delete the task
const deleteTask = (taskId) => {
  tasks.value.splice(taskId, 1)
}
</script>

<template>
  <h1 style="color: white; text-align: center">Todo List!</h1>

  <div class="todo-app">
    <div class="task-input">
      <input type="text" v-model="newTask" placeholder="Enter Task" />
      <button @click="addTask">Add task!</button>
    </div>

    <ul class="task-list" v-if="tasks.length > 0">
      <li class="task-item" v-for="(task, index) in tasks" :key="index">
        {{ task }}
        <button @click="deleteTask(index)">Remove</button>
      </li>
    </ul>

    <h4 v-else style="color: white; text-align: center">
      We're Sorted, No Pending Tasks, Enjoy! 🎉⭐
    </h4>
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

.todo-app {
  max-width: 400px;
  margin: 50px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.app-title {
  font-size: 24px;
  margin-bottom: 20px;
  text-align: center;
  color: #333;
}

.task-input {
  display: flex;
  gap: 10px;
}

input {
  flex: 1;
  padding: 8px;
  font-size: 14px;
}

button {
  padding: 8px 12px;
  font-size: 14px;
  background-color: #4caf50;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

.task-list {
  list-style: none;
  padding: 0;
}

.task-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  margin: 8px 0;
  background-color: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.remove-button {
  padding: 6px 10px;
  font-size: 12px;
  background-color: #e74c3c;
  color: #fff;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

.remove-button:hover {
  background-color: #c0392b;
}
</style>
