<template>
  <nav class="navbar">
    <div class="navbar-container">
      <div class="navbar-brand">Duelo Geek</div>
      <div class="navbar-links">
        <a href="#hero" class="nav-link">Início</a>
        <a href="#about" class="nav-link">Sobre</a>
        <a href="#community" class="nav-link">Comunidade</a>
        <a href="#products" class="nav-link">Produtos</a>
        <a href="#events" class="nav-link">Eventos</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
// Não precisa de RouterLink
</script>

<style scoped>
.navbar {
  background-color: var(--color-section-bg);
  padding: 1rem 0; /* 16px */
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
  border-bottom: 3px solid var(--color-main-highlight); /* Borda na cor principal */
}

.navbar-container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar-brand {
  color: var(--color-main-highlight); /* Dourado/Laranja */
  font-size: 2.25rem; /* 36px */
  font-weight: 800;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.6);
  letter-spacing: 1px;
}

.navbar-links {
  display: flex;
  gap: 1.5rem; /* 24px */
}

.nav-link {
  color: var(--color-text-muted);
  text-decoration: none;
  font-size: 1.1rem;
  font-weight: 600;
  padding: 0.6rem 1rem;
  border-radius: 8px;
  transition: all 0.3s ease-in-out;
  position: relative;
  overflow: hidden;
}

.nav-link::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
  transition: all 0.5s ease-in-out;
  z-index: 0;
}

.nav-link:hover::before {
  left: 100%;
}

.nav-link:hover {
  color: var(--color-text-light);
  transform: translateY(-2px) scale(1.02);
  background-color: rgba(255, 153, 0, 0.15); /* Laranja transparente no hover */
  box-shadow: 0 0 15px rgba(255, 153, 0, 0.4);
}

/* Responsividade */
@media (max-width: 768px) {
  .navbar-container {
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
  }

  .navbar-links {
    flex-direction: column;
    width: 100%;
    gap: 10px;
  }

  .nav-link {
    width: 100%;
    text-align: center;
    padding: 10px 0;
  }

  .navbar-brand {
    font-size: 2rem;
  }
}
</style>
