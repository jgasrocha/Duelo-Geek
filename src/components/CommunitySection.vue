<template>
  <section id="community" class="community-section section-base">
    <div class="container community-content">
      <h2 class="section-title">Nossa Vila Oculta da Comunidade</h2>
      <p class="section-text">
        Junte-se a uma vibrante comunidade de fãs, onde a força da amizade e a paixão por animes se encontram!
        Compartilhe suas coleções, participe de discussões épicas e faça novos amigos que entendem sua energia.
      </p>
      <div class="community-grid">
        <div class="community-item">
          <img :src="Discord" alt="Ícone de Fóruns" class="community-icon">
          <h3>Fóruns Saiyajin</h3>
          <p>Debates e teorias sobre seus universos favoritos.</p>
        </div>
        <div class="community-item">
          <img :src="Encontros" alt="Ícone de Eventos" class="community-icon">
          <h3>Encontros Ninja</h3>
          <p>Participe de lives, sorteios e torneios.</p>
        </div>
        <div class="community-item">
          <img :src="Duelo" alt="Ícone de Fanart" class="community-icon">
          <h3>Torneios e duelos</h3>
          <p>Mostre seu talento e ganhe prêmios.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import Duelo from '/duelo.png'
import Encontros from '/econtros.png'
import Discord from '/discord.jpg'
</script>

<style scoped>
.community-section {
  background-color: var(--color-dark-bg);
  padding: 80px 20px;
  border-bottom: 5px solid var(--color-main-highlight);
  text-align: center;
}

.section-title { /* herdado de style.css */ }
.section-title::after { /* herdado de style.css */ }
.section-text { /* herdado de style.css */ }

.community-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  margin-top: 40px;
}

.community-item {
  background-color: var(--color-card-bg);
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border: 1px solid var(--color-border);
}

.community-item:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.6);
  border-color: var(--color-main-highlight);
}

.community-icon {
  width: 100px;
  height: 100px;
  margin-bottom: 20px;
  border-radius: 50%;
  background-color: var(--color-accent-orange); /* Laranja de acento */
  padding: 10px;
  box-shadow: 0 0 20px rgba(249, 115, 22, 0.7);
  display: block;
  margin-left: auto;
  margin-right: auto;
  transition: all 0.3s ease;
}

.community-item:hover .community-icon {
  background-color: var(--color-main-highlight);
  box-shadow: 0 0 25px rgba(255, 153, 0, 0.8);
}

.community-item h3 {
  font-size: 1.8em;
  color: var(--color-text-light);
  margin-bottom: 10px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
}

.community-item p {
  font-size: 1em;
  color: var(--color-text-muted);
}

/* Responsividade */
@media (max-width: 768px) {
  .community-grid {
    grid-template-columns: 1fr;
  }
}
</style>
