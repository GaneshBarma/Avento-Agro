<template>
  <header class="app-bar">
    <div class="logo">
      <img src="@/assets/logo.png" alt="Avento-Agro Logo" class="logo-image" />
    </div>
    <nav class="nav-links">
      <router-link to="/" class="nav-link">Home</router-link>
      <router-link to="/products" class="nav-link">Products</router-link>
      <router-link to="/about" class="nav-link">About Us</router-link>
      <router-link to="/contact" class="nav-link">Contact</router-link>
    </nav>
  </header>
</template>

<script setup lang="ts">
</script>

<style scoped>
.app-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: var(--color-background);
  border-bottom: 1px solid var(--color-border);
  transition: background-color 0.5s, color 0.5s;
}

.logo {
  display: flex;
  align-items: center;
}

.logo-image {
  width: 100px;
  height: auto;
  margin-top: 1rem;
  margin-bottom: 1rem;
}

.logo-text {
  font-size: 1.5rem;
  color: var(--color-heading);
}

.nav-links {
  display: flex;
  gap: 1rem;
}

.nav-link {
  color: var(--color-text);
  text-decoration: none;
  font-size: 1rem;
  position: relative;
  transition: color 0.3s;
}

.nav-link::before {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 50%;
  width: 0;
  height: 2px;
  background-color: var(--color-border-hover);
  transition: width 0.3s ease, left 0.3s ease;
}

.nav-link:hover {
  color: var(--color-border-hover);
}

.nav-link:hover::before {
  width: 100%;
  left: 0;
}
</style>
