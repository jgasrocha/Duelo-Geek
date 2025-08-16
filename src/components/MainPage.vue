<template>
  <main class="main-content-area">
    <HeroSection />
    <AboutSection />
    <CommunitySection />
    <ProductSection />
    <EventSection />
    <Footer />
  </main>
</template>

<script setup>
import HeroSection from './HeroSection.vue';
import AboutSection from './AboutSection.vue';
import CommunitySection from './CommunitySection.vue';
import ProductSection from './ProductSection.vue';
import EventSection from './EventSection.vue';
import Footer from './Footer.vue';
</script>

<style scoped>
.main-content-area {
  flex-grow: 1;
  width: 100%;
}
</style>
