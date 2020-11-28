<template>
  <Hero :heroContent="heroContent" />
  <main>
    <Category :wines="drinkAgain" heading="Drink Again" />
    <Category :wines="keepDrinking" heading="Keep Drinking" />
  </main>
</template>

<script>
import Category from './components/Category.vue';
import Hero from './components/Hero.vue';

export default {
  name: 'App',
  components: {
    Category,
    Hero,
  },
  computed: {
    heroContent() {
      return {
        title: 'Rex Goliath',
        subtitle: 'His Royal Majesty is back.',
        imageUrl: '/rex-goliath-logo.png',
        description: `America's most unhinged rooster is out of retirement, and this time? He's mad
        as hell.  Experience the unapologetic flavor burst of Rex Goliath.`,
      };
    },
    wines() {
      return [{
        id: 1,
        imageUrl: '/red-wine.jpg',
        isNew: true,
        label: 'Wine',
        isFinished: true,
      }, {
        id: 2,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isFinished: true,
      }, {
        id: 3,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isNew: true,
        isFinished: true,
      }, {
        id: 4,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isFinished: true,
      }, {
        id: 5,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isNew: true,
        isFinished: true,
      }, {
        id: 6,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isFinished: true,
      }, {
        id: 7,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isFinished: true,
      }, {
        id: 8,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isFinished: true,
      }, {
        id: 1,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 2,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 3,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 4,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 5,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 6,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 7,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }, {
        id: 8,
        imageUrl: '/red-wine.jpg',
        progress: 22,
        label: 'Wine',
      }];
    },
    drinkAgain() {
      return this.wines.filter((wine) => wine.isFinished);
    },
    keepDrinking() {
      return this.wines.filter((wine) => wine.progress);
    },
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Fira+Sans:wght@400;700&display=swap");

img {
  max-width: 100%;
}
a {
  color: inherit;
  text-decoration: none;
}
body {
  font-family: "Fira Sans", sans-serif;
  background-color: hsl(0, 0%, 10%);
}

main {
  padding: 18px 48px;
  margin-top: -72px;
}
</style>
