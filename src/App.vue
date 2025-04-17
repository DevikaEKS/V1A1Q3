<script setup>
import { ref, onMounted } from 'vue';
const products = ref([]);
onMounted(async () => {
  try {
    const res = await fetch('https://fakestoreapi.com/products');
    const data = await res.json();
    products.value = data;
  } catch (error) {
    console.error("Error fetching products:", error);
  }
});
</script>
<template>
  <main>
    <div class="product-container">
      <h2 class="product-title">Featured Products</h2>
      <div class="product-grid">
        <div
          v-for="product in products"
          :key="product.id"
          class="product-card"
        >
          <img class="product-image" :src="product.image" :alt="product.title" />
          <h4 class="product-name">{{ product.title }}</h4>
          <p class="product-price">${{ product.price }}</p>
        </div>
      </div>
    </div>
  </main>
</template>
