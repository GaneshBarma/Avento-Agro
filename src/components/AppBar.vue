<template>
  <Menubar :model="items">
    <template #start>
      <router-link to="/" class="logo">Avento-Agro</router-link>
    </template>
  </Menubar>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
import Menubar from 'primevue/menubar';

const router = useRouter();
const items = ref([
  { label: 'Home', command: () => router.push('/') },
  { label: 'Products', command: () => router.push('/products') },
  { label: 'About', command: () => router.push('/about') },
  { label: 'Contact', command: () => router.push('/contact') }
]);
</script>

<style scoped>
.logo {
  font-size: 1.5rem;
  color: white;
  text-decoration: none;
}

.p-menubar {
  background-color: #4CAF50;
}

.p-menubar-root-list > .p-menuitem > .p-menuitem-link {
  color: white;
}

.p-menubar-root-list > .p-menuitem > .p-menuitem-link:hover {
  background-color: #45a049;
}
</style>
