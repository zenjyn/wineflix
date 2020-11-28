<template>
  <div class="hero-content">
    <h2><img alt="Rex Goliath" src="/rex-goliath-logo.png" /></h2>
    <h3>His Royal Majesty is back.</h3>
    <p>America's most unhinged rooster is out of retirement, and this time? He's mad as hell.
  Experience the unapologetic flavor burst of Rex Goliath.</p>
    <Controls />
  </div>
</template>

<script>
import Controls from './Controls.vue';

export default {
  name: 'HeroContent',
  components: {
    Controls,
  },
};
</script>

<style lang="scss">
.hero-content {
  margin-top: 200px;
  margin-bottom: 200px;
  h3 {
    margin-top: 24px;
    margin-bottom: 24px;
    font-size: 30px;
    font-weight: 700;
    text-shadow: 1px 1px 1px hsl(0, 0, 20%);
  }
  p {
    font-size: 24px;
    margin-bottom: 24px;
    max-width: 600px;
    line-height: 1.4;
  }
}
</style>
