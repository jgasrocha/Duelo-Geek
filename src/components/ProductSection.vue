<template>
  <section id="products" class="products-section section-base">
    <div class="container product-content">
      <h2 class="section-title">Tesouros do Mundo Geek</h2>
      <p class="section-text">
        Desvende o poder dos nossos produtos! Explore uma vasta seleção de itens licenciados,
        feitos para verdadeiros colecionadores e fãs apaixonados. Qual será o seu próximo tesouro?
      </p>
      <div class="product-grid">
        <div class="product-card">
          <img :src="Goku" alt="Action Figure do Goku" class="product-image">
          <h3>Action Figures Lendárias</h3>
          <p>De Dragon Ball a Naruto, os maiores heróis e vilões em detalhes incríveis.</p>
        </div>
        <div class="product-card">
          <img :src="Placa" alt="Mangá de Naruto" class="product-image">
          <h3>Placas Decorativas</h3>
          <p>Decore seu espaço geek com as placas dos seus animes favoritos. Perfeitas para fãs!</p>
        </div>
        <div class="product-card">
          <img :src="Camisa" alt="Camisa Anime" class="product-image">
          <h3>Vestuário Exclusivo</h3>
          <p>Mostre seu estilo ninja ou guerreiro Saiyajin.</p>
        </div>
        <div class="product-card">
          <img :src="Colecionavel" alt="Funko Pop" class="product-image">
          <h3>Colecionáveis Raros</h3>
          <p>Funko Pops, estátuas e edições limitadas.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import Goku from'/gokuaction.png'
import Camisa from '/camisa1.png'
import Colecionavel from '/colecionavel.png'
import Placa from '/narutoplaca.png'

</script>

<style scoped>
.products-section {
  background-color: var(--color-section-bg);
  padding: 80px 20px;
  border-bottom: 5px solid var(--color-main-highlight);
  text-align: center;
}

.section-title { /* herdado de style.css */ }
.section-title::after { /* herdado de style.css */ }
.section-text { /* herdado de style.css */ }

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  margin-top: 40px;
}

.product-card {
  background-color: var(--color-card-bg);
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
  overflow: hidden;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
  border: 1px solid var(--color-border);
}

.product-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.6);
  border-color: var(--color-accent-orange); /* Borda laranja no hover */
}

.product-image {
  width: 100%;
  height: 300px;
  object-fit: cover;
  border-bottom: 1px solid var(--color-border);
}

.product-card h3 {
  font-size: 1.6em;
  color: var(--color-text-light);
  margin: 15px 0 10px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
}

.product-card p {
  font-size: 0.95em;
  color: var(--color-text-muted);
  padding-bottom: 15px;
}

/* Responsividade */
@media (max-width: 768px) {
  .product-grid {
    grid-template-columns: 1fr;
  }
}
</style>