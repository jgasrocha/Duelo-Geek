<template>
  <section id="events" class="events-section section-base">
    <div class="container event-content">
      <h2 class="section-title">Calendário de Batalhas e Festivais</h2>
      <p class="section-text">
        Prepare-se para eventos épicos! De lançamentos exclusivos a torneios que testarão suas habilidades,
        o Duelo Geek tem sempre algo acontecendo.
      </p>
      <div class="event-cards">
        <div class="event-card">
          <h3>Lançamento Exclusivo: O Novo Mangá de Konoha</h3>
          <p>Data: 25 de Agosto de 2025</p>
          <p>Local: Online & Loja Física</p>
          <button class="event-button">Inscrever-se</button>
        </div>
        <div class="event-card">
          <h3>Torneio de Card Game: Batalha de Saiyajins!</h3>
          <p>Data: 10 de Setembro de 2025</p>
          <p>Local: Centro de Treinamento Geek</p>
          <button class="event-button">Detalhes</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Nenhuma lógica específica de script para este componente no momento
</script>

<style scoped>
.events-section {
  background-color: var(--color-dark-bg);
  padding: 80px 20px;
  border-bottom: 5px solid var(--color-accent-orange);
  text-align: center;
}

.section-title { /* herdado de style.css */ }
.section-title::after { /* herdado de style.css */ }
.section-text { /* herdado de style.css */ }

.event-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 30px;
  margin-top: 40px;
}

.event-card {
  background-color: var(--color-card-bg);
  padding: 30px;
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  border: 1px solid var(--color-border);
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
}

.event-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.6);
  border-color: var(--color-main-highlight);
}

.event-card h3 {
  font-size: 1.8em;
  color: var(--color-text-light);
  margin-bottom: 15px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
}

.event-card p {
  font-size: 1.1em;
  color: var(--color-text-muted);
  margin-bottom: 10px;
}

.event-button {
  background-image: linear-gradient(to right, var(--color-main-highlight), var(--color-accent-orange));
  color: var(--color-text-light);
  padding: 14px 30px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 1.2em;
  font-weight: bold;
  margin-top: 20px;
  transition: all 0.3s ease-in-out;
  align-self: flex-start;
  box-shadow: 0 4px 15px rgba(255, 153, 0, 0.5);
  text-transform: uppercase;
}

.event-button:hover {
  background-image: linear-gradient(to right, var(--color-accent-orange), var(--color-main-highlight));
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 8px 20px rgba(255, 153, 0, 0.7);
  filter: brightness(1.1);
}

/* Responsividade */
@media (max-width: 768px) {
  .event-cards {
    grid-template-columns: 1fr;
  }
}
</style>