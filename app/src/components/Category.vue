<template>
  <section class="category">
    <h2>{{ heading }}</h2>
    <ul>
      <li v-for="wine in wines" :key="wine.id">
        <Wine
          :imageUrl="wine.imageUrl"
          :progress="wine.progress"
          :isNew="wine.isNew"
          :label="wine.label"
        />
      </li>
    </ul>
  </section>
</template>

<script>
import Wine from './Wine.vue';

export default {
  name: 'Category',
  components: {
    Wine,
  },
  props: {
    wines: Array,
    heading: String,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Fira+Sans:wght@400;700&display=swap");

.category {
  margin-bottom: 16px;
  h2 {
    color: #fff;
    font-size: 32px;
    font-weight: 400;
    margin-bottom: 20px;
  }
  ul {
    display: flex;
    flex-flow: row nowrap;
    overflow-x: auto;
  }
}
</style>
