<template>
  <header class="hero">
    <img class="hero-image" src="/wine-hero.webp">
    <AppNavigation :navigationLinks="navigationLinks" />
    <HeroContent />
  </header>
</template>

<script>
import AppNavigation from '@/components/AppNavigation.vue';
import HeroContent from '@/components/HeroContent.vue';

export default {
  name: 'AppHeader',
  components: {
    AppNavigation,
    HeroContent,
  },
  props: {
    navigationLinks: Array,
  },
};
</script>
