<template>
  <header class="hero">
    <HeroImage />
    <Navigation />
    <HeroContent
      :title="heroContent.title"
      :subtitle="heroContent.subtitle"
      :imageUrl="heroContent.imageUrl"
      :description="heroContent.description"
    />
  </header>
</template>

<script>
import HeroImage from './HeroImage.vue';
import HeroContent from './HeroContent.vue';
import Navigation from './Navigation.vue';

export default {
  name: 'Hero',
  components: {
    HeroImage,
    HeroContent,
    Navigation,
  },
  props: {
    heroContent: Object,
  },
};
</script>

<style lang="scss">
.hero {
  position: relative;
  color: #fff;
  overflow-y: hidden;
  nav, .hero-content {
    padding: 18px 48px;
  }
}
</style>
