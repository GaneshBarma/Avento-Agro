<template>
  <div id="app">
    <AppBar />
    <RouterView />
  </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router';
import AppBar from './components/AppBar.vue';
</script>

<style scoped>
</style>
