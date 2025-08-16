<template>
  <footer class="footer">
    <p>&copy; 2025 Duelo Geek. Todos os direitos reservados. Com paixão pelos animes!</p>
    <!-- <div class="social-links">
      <a href="#" class="social-icon">F</a>
      <a href="#" class="social-icon">I</a>
      <a href="#" class="social-icon">T</a>
    </div> -->
  </footer>
</template>

<script setup>
// Nenhuma lógica específica de script para este componente no momento
</script>

<style scoped>
.footer {
  background-color: var(--color-section-bg);
  color: var(--color-text-muted);
  text-align: center;
  padding: 40px 20px;
  font-size: 0.95em;
  border-top: 5px solid var(--color-main-highlight);
}

.social-links {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  gap: 15px;
}

.social-icon {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 45px;
  height: 45px;
  background-color: var(--color-dark-bg);
  color: var(--color-main-highlight);
  border-radius: 50%;
  text-decoration: none;
  font-size: 1.4em;
  font-weight: bold;
  transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.4);
  border: 2px solid var(--color-border);
}

.social-icon:hover {
  background-color: var(--color-main-highlight);
  color: var(--color-text-light);
  transform: translateY(-5px) scale(1.1);
  box-shadow: 0 8px 20px rgba(255, 153, 0, 0.6);
  border-color: var(--color-main-highlight);
}
</style>