<script setup>
import ProductCard from "@/components/ProductCard.vue";

const products = [
  {
    id: 1,
    name: "Laptop",
    price: 999.99,
    image:
      "https://macshack.co.za/cdn/shop/files/MacBookAir13-inchM3SpaceGray.001_c416f697-c327-4387-8fe5-17d2effada2f.jpg",
  },
  {
    id: 2,
    name: "Headphones",
    price: 599.9,
    image: "https://www.emirates.store/media/11553/headphone1_p.jpg",
  },
  {
    id: 3,
    name: "Smartphone",
    price: 699.99,
    image:
      "https://www.pngkey.com/png/detail/774-7746455_buy-the-new-samsung-galaxy-samsung.png",
  },
  {
    id: 1,
    name: "Laptop",
    price: 999.99,
    image:
      "https://macshack.co.za/cdn/shop/files/MacBookAir13-inchM3SpaceGray.001_c416f697-c327-4387-8fe5-17d2effada2f.jpg",
  },
  {
    id: 2,
    name: "Headphones",
    price: 599.9,
    image: "https://www.emirates.store/media/11553/headphone1_p.jpg",
  },
  {
    id: 3,
    name: "Smartphone",
    price: 699.99,
    image:
      "https://www.pngkey.com/png/detail/774-7746455_buy-the-new-samsung-galaxy-samsung.png",
  },
  {
    id: 1,
    name: "Laptop",
    price: 999.99,
    image:
      "https://macshack.co.za/cdn/shop/files/MacBookAir13-inchM3SpaceGray.001_c416f697-c327-4387-8fe5-17d2effada2f.jpg",
  },
  {
    id: 2,
    name: "Headphones",
    price: 599.9,
    image: "https://www.emirates.store/media/11553/headphone1_p.jpg",
  },
  {
    id: 3,
    name: "Smartphone",
    price: 699.99,
    image:
      "https://www.pngkey.com/png/detail/774-7746455_buy-the-new-samsung-galaxy-samsung.png",
  },
  {
    id: 1,
    name: "Mi Notebook Laptop",
    offerPrice: 599.9,
    price: 999.99,
    image:
      "https://macshack.co.za/cdn/shop/files/MacBookAir13-inchM3SpaceGray.001_c416f697-c327-4387-8fe5-17d2effada2f.jpg",
  },
  {
    id: 2,
    name: "Headphones",
    price: 599.9,
    image: "https://www.emirates.store/media/11553/headphone1_p.jpg",
  },
  {
    id: 3,
    name: "Smartphone",
    price: 699.99,
    image:
      "https://www.pngkey.com/png/detail/774-7746455_buy-the-new-samsung-galaxy-samsung.png",
  },
];

function addToCart(productName) {
  console.log(productName);
  // sending the data to backend api
  alert(`Product has been added to cart! - ${productName}`);
}
</script>

<template>
  <h1>Emax - Products App!</h1>
  <p>to demostrate use of props in vue js!</p>

  <!-- product List -->

  <div class="products">
    <ProductCard
      v-for="product in products"
      :key="product.id"
      :image="product.image"
      :price="product.price"
      :offerPrice="product.offerPrice"
      :name="product.name"
      desc="something very very random."
      @productName="addToCart"
    />
  </div>
</template>

<style>
.products {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}

.productCard {
  width: 300px;
  border: 1px solid lightgray;
  border-radius: 7px;
  text-align: center;
  padding: 1rem;
  margin: 1rem;
}
</style>
