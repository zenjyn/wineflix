<template>
  <div class="hero-content">
    <h2><img :alt="title" :src="imageUrl" /></h2>
    <h3>{{subtitle}}</h3>
    <p>{{description}}</p>
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
  props: {
    title: String,
    imageUrl: String,
    subtitle: String,
    description: String,
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
