<template>
    <nav class="navbar">
      <div class="container">
        <a class="logo" href="/">Avento-Agro</a>
        <ul class="nav-links">
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/products">Products</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script lang="ts" setup>
  </script>
  
  <style scoped>
  .navbar {
    background-color: #4CAF50;
    padding: 1rem;
  }
  .logo {
    color: white;
    text-decoration: none;
    font-size: 1.5rem;
  }
  .nav-links {
    list-style: none;
    display: flex;
    gap: 1rem;
  }
  .nav-links a {
    color: white;
    text-decoration: none;
  }
  </style>
  