<template>
  <nav class="navbar">
    <div class="navbar-container">
      <div class="navbar-brand">Duelo Geek</div>

      <!-- Botão do menu hamburguer (visível apenas em telas pequenas) -->
      <button class="hamburger-menu" @click="toggleMobileMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>

      <!-- Links da navegação -->
      <div :class="['navbar-links', { 'active': showMobileMenu }]">
        <a href="#hero" class="nav-link" @click="hideMobileMenu">Início</a>
        <a href="#about" class="nav-link" @click="hideMobileMenu">Sobre</a>
        <a href="#community" class="nav-link" @click="hideMobileMenu">Comunidade</a>
        <a href="#products" class="nav-link" @click="hideMobileMenu">Produtos</a>
        <a href="#events" class="nav-link" @click="hideMobileMenu">Eventos</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

// Estado para controlar a visibilidade do menu móvel
const showMobileMenu = ref(false);

// Função para alternar a visibilidade do menu
const toggleMobileMenu = () => {
  showMobileMenu.value = !showMobileMenu.value;
};

// Função para esconder o menu após clicar em um link (opcional, para melhor UX)
const hideMobileMenu = () => {
  showMobileMenu.value = false;
};
</script>

<style scoped>
.navbar {
  background-color: var(--color-section-bg);
  padding: 1rem 0;
  /* 16px */
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
  border-bottom: 3px solid var(--color-main-highlight);
  /* Borda na cor principal */
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
  color: var(--color-main-highlight);
  /* Dourado/Laranja */
  font-size: 2.25rem;
  /* 36px */
  font-weight: 800;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.6);
  letter-spacing: 1px;
}

/* Estilos para o botão do menu hamburguer */
.hamburger-menu {
  display: none;
  /* Escondido por padrão em telas maiores */
  flex-direction: column;
  justify-content: space-around;
  width: 30px;
  height: 25px;
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 1001;
  /* Garante que fique acima dos links */
}

.hamburger-menu .bar {
  width: 100%;
  height: 3px;
  background-color: var(--color-main-highlight);
  /* Cor da barra */
  border-radius: 5px;
  transition: all 0.3s ease-in-out;
}

/* Animação do hamburguer para X */
.hamburger-menu.active .bar:nth-child(1) {
  transform: translateY(11px) rotate(45deg);
}

.hamburger-menu.active .bar:nth-child(2) {
  opacity: 0;
}

.hamburger-menu.active .bar:nth-child(3) {
  transform: translateY(-11px) rotate(-45deg);
}


/* Links da navegação */
.navbar-links {
  display: flex;
  gap: 1.5rem;
  /* 24px */
  transition: all 0.3s ease-in-out;
  /* Transição para o menu */
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
  background-color: rgba(255, 153, 0, 0.15);
  /* Laranja transparente no hover */
  box-shadow: 0 0 15px rgba(255, 153, 0, 0.4);
}

/* Responsividade para telas menores */
@media (max-width: 768px) {
  .hamburger-menu {
    display: flex;
    /* Mostra o hamburguer em telas pequenas */
  }

  .navbar-links {
    flex-direction: column;
    position: absolute;
    top: 100%;
    /* Abaixo do navbar */
    left: 0;
    width: 100%;
    background-color: var(--color-section-bg);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4);
    padding: 15px 0;
    opacity: 0;
    /* Esconde o menu por padrão */
    visibility: hidden;
    transform: translateY(-10px);
  }

  .navbar-links.active {
    opacity: 1;
    /* Mostra o menu quando ativo */
    visibility: visible;
    transform: translateY(0);
  }

  .nav-link {
    width: 100%;
    text-align: center;
    padding: 12px 0;
    font-size: 1.2rem;
  }

  .navbar-brand {
    font-size: 2rem;
  }
}
</style>