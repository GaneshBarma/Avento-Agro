<template>
  <div id="app">
    <AppBar />
    <main class="main-content">
      <transition name="fade" mode="out-in">
        <RouterView />
      </transition>
    </main>
    <FooterBar />
  </div>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppBar from './components/AppBar.vue'
import FooterBar from './components/FooterBar.vue'
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
}

.main-content {
  flex: 1;
}
</style>
