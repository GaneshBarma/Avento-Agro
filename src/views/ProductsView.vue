<template>
  <div class="products">
    <h1>Our Products</h1>
    <p>Explore our range of agricultural products.</p>
    <div class="product-list">
      <div class="product-card" v-for="product in products" :key="product.id">
        <img :src="product.image" :alt="product.name" class="product-image" />
        <h2 class="product-name">{{ product.name }}</h2>
        <p class="product-description">{{ product.description }}</p>
        <p class="product-price">{{ formatPrice(product.price) }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

// Sample product data
const products = ref([
  {
    id: 1,
    name: 'Organic Fertilizer',
    description: 'High-quality organic fertilizer for sustainable farming.',
    price: 1499.99,
    image: 'https://via.placeholder.com/150',
  },
  {
    id: 2,
    name: 'Hybrid Seeds',
    description: 'Top-grade hybrid seeds for better yield.',
    price: 999.99,
    image: 'https://via.placeholder.com/150',
  },
  {
    id: 3,
    name: 'Agricultural Tools',
    description: 'Durable tools for all your farming needs.',
    price: 2499.99,
    image: 'https://via.placeholder.com/150',
  },
]);

// Function to format price in rupees
const formatPrice = (price: number) => {
  return `₹${price.toFixed(2)}`;
};
</script>

<style scoped>
.products {
  text-align: center;
  margin-top: 2rem;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  margin-top: 2rem;
}

.product-card {
  background-color: var(--color-background-soft);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: 1rem;
  width: 200px;
  transition: transform 0.3s;
}

.product-card:hover {
  transform: scale(1.05);
}

.product-image {
  width: 100%;
  height: auto;
  border-radius: 4px;
}

.product-name {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

.product-description {
  font-size: 0.875rem;
  color: var(--color-text);
}

.product-price {
  font-size: 1rem;
  color: var(--color-heading);
  margin-top: 0.5rem;
}
</style>
