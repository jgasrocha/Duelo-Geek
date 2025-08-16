<template>
  <div class="app-container">
    <Navbar />
    <MainPage />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import MainPage from './components/MainPage.vue'
</script>

<style>
.app-container {
  min-height: 100vh;
  background-color: var(--color-dark-bg); /* Fundo base para o app */
}
</style>
