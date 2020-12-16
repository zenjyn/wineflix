<template>
  <header class="hero">
    <img class="hero-image" src="/wine-hero.webp">
    <Navigation :navigationLinks="navigationLinks" />
    <HeroContent />
  </header>
</template>

<script>
import Navigation from '@/components/Navigation.vue';
import HeroContent from '@/components/HeroContent.vue';

export default {
  name: 'Header',
  components: {
    HeroContent,
    Navigation,
  },
  props: {
    navigationLinks: Array,
  },
};
</script>
