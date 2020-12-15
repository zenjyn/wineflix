<template>
  <header class="hero">
    <img class="hero-image" src="/wine-hero.webp">
    <nav class="navigation">
      <section class="primary-navigation">
        <h1>WineFlix</h1>
        <Navigation />
      </section>
      <section class="secondary-navigation">
        <UserAvatar link="#" label="S" />
      </section>
    </nav>
    <HeroContent />
  </header>
</template>

<script>
import HeroContent from '@/components/HeroContent.vue';
import Navigation from '@/components/Navigation.vue';
import UserAvatar from '@/components/UserAvatar.vue';

export default {
  name: 'Header',
  components: {
    HeroContent,
    Navigation,
    UserAvatar,
  },
};
</script>
