<template>
  <section id="hero" class="hero-section section-base">
    <div class="container hero-content">
      <h1 class="hero-title">Duelo Geek: Sua Aventura Começa Aqui!</h1>
      <p class="hero-description">
        No Duelo Geek, transformamos sua paixão por animes, mangás e colecionáveis em realidade.
        Somos mais que uma loja, somos o seu portal para um universo de produtos autênticos e raridades.
        Descubra figuras de ação, mangás, roupas e acessórios que celebram seus personagens favoritos.
        Prepare-se para o duelo de coleções!
      </p>
      <button class="hero-button">Explorar Produtos</button>
    </div>
  </section>
</template>

<script setup>
// Sem lógica adicional por enquanto
</script>

<style scoped>
.hero-section {
  min-height: 700px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  background-image: linear-gradient(rgba(17, 24, 39, 0.8), rgba(17, 24, 39, 0.8)), url('/luffy.jpg');
  background-size: cover;
  background-position: center;
  text-align: center;
  padding: 80px 20px;
  border-bottom: 5px solid var(--color-main-highlight); /* Borda laranja-amarelada */
}

.hero-content {
  max-width: 900px;
  color: var(--color-text-light);
  position: relative;
  z-index: 1;
}

.hero-title {
  font-size: 4.8em;
  margin-bottom: 30px;
  text-shadow: 4px 4px 8px rgba(0, 0, 0, 0.8);
  font-weight: 900;
  color: var(--color-main-highlight);
  line-height: 1.1;
  letter-spacing: 2px;
}

.hero-description {
  font-size: 1.8em;
  line-height: 1.8;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.6);
  color: var(--color-text-muted);
  max-width: 800px;
  margin: 0 auto 50px;
}

.hero-button {
  background-image: linear-gradient(to right, var(--color-main-highlight), var(--color-accent-orange));
  color: var(--color-text-light);
  padding: 18px 45px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  font-size: 1.4em;
  font-weight: bold;
  transition: all 0.3s ease-in-out;
  box-shadow: 0 6px 20px rgba(255, 153, 0, 0.5);
  text-transform: uppercase;
  letter-spacing: 1px;
}

.hero-button:hover {
  background-image: linear-gradient(to right, var(--color-accent-orange), var(--color-main-highlight));
  transform: translateY(-8px) scale(1.05);
  box-shadow: 0 12px 30px rgba(255, 153, 0, 0.7);
  filter: brightness(1.1);
}

/* Responsividade */
@media (max-width: 1024px) {
  .hero-title {
    font-size: 4em;
  }
  .hero-description {
    font-size: 1.5em;
  }
}

@media (max-width: 768px) {
  .hero-section {
    min-height: 500px;
    padding: 60px 15px;
  }
  .hero-title {
    font-size: 3.2em;
  }
  .hero-description {
    font-size: 1.2em;
  }
  .hero-button {
    padding: 15px 35px;
    font-size: 1.2em;
  }
}

@media (max-width: 480px) {
  .hero-section {
    min-height: 400px;
    padding: 40px 10px;
  }
  .hero-title {
    font-size: 2.5em;
  }
  .hero-description {
    font-size: 1em;
  }
}
</style>
