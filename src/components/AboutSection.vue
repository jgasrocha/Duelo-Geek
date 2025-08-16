<template>
  <section id="about" class="about-section section-base">
    <div class="container about-content">
      <h2 class="section-title">Sobre o Duelo Geek</h2>
      <p class="section-text">
        No Duelo Geek, somos fãs apaixonados por anime e cultura pop, assim como você!
        Nossa missão é trazer os melhores produtos diretamente do universo dos seus personagens favoritos.
        Desde figuras de ação detalhadas até mangás e colecionáveis raros, cada item é selecionado com carinho
        para garantir que sua coleção seja lendária. Junte-se à nossa jornada e descubra um tesouro a cada clique!
      </p>
      <div class="about-cards">
        <div class="about-card">
          <h3>Qualidade Superior</h3>
          <p>Produtos autênticos e de alta durabilidade.</p>
        </div>
        <div class="about-card">
          <h3>Entrega Rápida</h3>
          <p>Seus itens chegam prontos para a batalha.</p>
        </div>
        <div class="about-card">
          <h3>Suporte Kamehameha</h3>
          <p>Atendimento dedicado para suas dúvidas.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Sem lógica adicional por enquanto
</script>

<style scoped>
.about-section {
  background-color: var(--color-section-bg);
  padding: 80px 20px;
  border-bottom: 5px solid var(--color-accent-orange); /* Borda laranja */
  text-align: center;
}

.section-title { /* herdado de style.css */ }
.section-title::after { /* herdado de style.css */ }
.section-text { /* herdado de style.css */ }

.about-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  margin-top: 40px;
}

.about-card {
  background-color: var(--color-card-bg);
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border: 1px solid var(--color-border);
}

.about-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.6);
  border-color: var(--color-main-highlight); /* Borda laranja-amarelada no hover */
}

.about-card h3 {
  font-size: 1.8em;
  color: var(--color-main-highlight);
  margin-bottom: 15px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
}

.about-card p {
  font-size: 1em;
  color: var(--color-text-muted);
}

/* Responsividade */
@media (max-width: 768px) {
  .about-cards {
    grid-template-columns: 1fr;
  }
}
</style>