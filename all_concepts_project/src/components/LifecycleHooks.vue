<script setup>
import { onMounted, onUnmounted } from "vue";

// In Vue 3, lifecycle hooks are methods that allow you to hook into different stages of a component's lifecycle, from creation to destruction. Here's a quick overview of the key lifecycle hooks in Vue 3:

// setup: Called before the component is created. It's where you set up reactive state, computed properties, and methods using the Composition API.

// onBeforeMount: Called right before the component is mounted to the DOM. Useful for operations that need to happen right before the component appears.

// onMounted: Called after the component is mounted. Ideal for performing operations that need to interact with the DOM or perform async tasks once the component is fully rendered.

// onBeforeUpdate: Called before the component’s reactive data changes and the DOM updates. Use this for any cleanup or preparation before an update occurs.

// onUpdated: Called after the component’s reactive data has changed and the DOM has updated. Useful for operations that need to occur after the DOM has been updated.

// onBeforeUnmount: Called right before the component is unmounted from the DOM. Useful for cleanup activities like removing event listeners or cancelling network requests.

// onUnmounted: Called after the component has been unmounted from the DOM. Final cleanup or teardown operations are typically performed here.

// onErrorCaptured: Called when an error is captured from a descendant component. Use this to handle errors and prevent them from propagating further.

onMounted(() => {
  console.log("Component is mounted!");
});

onUnmounted(() => {
  console.log("Component is destroyed!");
});

</script>

<template>
  <h1>Lifecycle hooks</h1>
</template>
