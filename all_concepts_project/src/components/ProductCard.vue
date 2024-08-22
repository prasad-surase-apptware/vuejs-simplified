<script setup>
import { defineProps } from "vue";

const { image, price, name, desc, offerPrice } = defineProps({
  image: {},
  price: {
    type: Number,
    validator: (value) => value > 100,
  },
  name: {
    required: true,
  },
  desc: {},
  offerPrice: {},
});
</script>

<template>
  <div class="productCard">
    <img width="300px" :src="image" alt="soap" />

    <p>Price: {{ price }}</p>

    <p v-if="offerPrice" style="color: green">Offer Price: {{ offerPrice }}</p>

    <h3>{{ name }}</h3>

    <p>
      {{ desc }}
    </p>
    <button class="btn" @click="$emit('productName', name)">Buy Now!</button>
  </div>
</template>
