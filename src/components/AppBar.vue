<template>
  <Menubar :model="items">
    <template #start>
      <router-link to="/" class="logo-link">
        <img src="@/assets/Logo.png" alt="Avento-Agro Logo" class="logo" @click="router.push('/')"/>
      </router-link>
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
  height: 4.5rem;
  width: auto;
  /* color: white;
  text-decoration: none; */
}

.logo-link {
  display: flex;
  align-items: center;
  height: 100%;
}

.p-menubar {
  /* background-color: #4CAF50; */
}

.p-menubar-root-list > .p-menuitem > .p-menuitem-link {
  color: white;
}

.p-menubar-root-list > .p-menuitem > .p-menuitem-link:hover {
  background-color: #45a049;
}
</style>
