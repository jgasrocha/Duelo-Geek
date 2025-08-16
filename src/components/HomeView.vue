<template>
  <div class="home-content">
    <h1 class="home-title">Bem-vindo ao Duelo Geek</h1>
    <p class="home-subtitle">Seu portal para as últimas novidades e discussões sobre o mundo dos animes.</p>
    <img src="https://via.placeholder.com/800x400.png?text=Duelo+Geek" alt="Imagem Duelo Geek" class="home-image">
  </div>
</template>

<script setup>
// Sem lógica adicional por enquanto
</script>

<style scoped>
.home-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 48px 16px;
  text-align: center;
}

.home-title {
  font-size: 36px;
  font-weight: bold;
  color: #fff;
  margin-bottom: 16px;
}

.home-subtitle {
  font-size: 18px;
  color: #a0aec0; /* Cor de texto cinza, equivalente ao gray-300 */
}

.home-image {
  margin-top: 32px;
  max-width: 100%;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>