<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-left">
        <img src="@/assets/logo.png" alt="Avento-Agro Logo" class="logo-image" />
        <address class="corporate-info">
          <p>Avento-Agro Corporate Office</p>
          <p>Nagole</p>
          <p>Phone: +123 456 7890</p>
          <p>Email: contact@avento-agro.com</p>
        </address>
      </div>
      <div class="footer-right">
        <h3>Quick Links</h3>
        <nav class="quick-links">
          <router-link to="/">Home</router-link>
          <router-link to="/products">Products</router-link>
          <router-link to="/about">About Us</router-link>
          <router-link to="/contact">Contact</router-link>
        </nav>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; {{ currentYear }} Avento-Agro. All rights reserved.</p>
    </div>
  </footer>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

// Get the current year for the footer
const currentYear = new Date().getFullYear();
</script>

<style scoped>
.footer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: var(--color-background-soft);
  padding: 1rem 0;
  border-top: 1px solid var(--color-border);
  width: 100%;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  width: 100%;
  max-width: 1200px;
  padding: 1rem;
}

.footer-left {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.logo-image {
  width: 100px;
  height: auto;
  margin-bottom: 1rem;
}

.corporate-info {
  font-style: normal;
  line-height: 1.6;
  color: var(--color-text);
}

.footer-right {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.footer-right h3 {
  margin-bottom: 0.5rem;
  color: var(--color-heading);
}

.quick-links {
  display: flex;
  flex-direction: column;
}

.quick-links a {
  color: var(--color-text);
  text-decoration: none;
  margin-bottom: 0.5rem;
  transition: color 0.3s;
}

.quick-links a:hover {
  color: var(--color-border-hover);
}

.footer-bottom {
  text-align: center;
  margin-top: 1rem;
  color: var(--color-text);
}

.footer-bottom p {
  margin: 0.5rem 0;
}
</style>
