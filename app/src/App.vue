<template>
  <header class="hero">
    <HeroImage />
    <nav>
      <section class="primary-navigation">
        <Logo />
        <NavigationLinks />
      </section>
      <section class="secondary-navigation">
        <a href="#"><span class="user-logo">S</span></a>
      </section>
    </nav>
    <div class="hero-content">
      <h2><img alt="Rex Goliath" src="/rex-goliath-logo.png" /></h2>
      <h3>His Royal Majesty is back.</h3>
      <p>America's most unhinged rooster is out of retirement, and this time? He's mad as hell.
    Experience the unapologetic flavor burst of Rex Goliath.</p>
      <Controls />
    </div>
  </header>
  <main>
    <Category :wines="drinkAgain" heading="Drink Again" />
    <Category :wines="keepDrinking" heading="Keep Drinking" />
  </main>
</template>

<script>
import Logo from './components/Logo.vue';
import HeroImage from './components/HeroImage.vue';
import Category from './components/Category.vue';
import Controls from './components/Controls.vue';
import NavigationLinks from './components/NavigationLinks.vue';

export default {
  name: 'App',
  components: {
    Logo,
    HeroImage,
    Category,
    Controls,
    NavigationLinks,
  },
  computed: {
    drinkAgain() {
      return [{
        id: 1,
        imageUrl: '/red-wine.jpg',
        isNew: true,
        label: 'Wine',
      }, {
        id: 2,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
      }, {
        id: 3,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isNew: true,
      }, {
        id: 4,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
      }, {
        id: 5,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
        isNew: true,
      }, {
        id: 6,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
      }, {
        id: 7,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
      }, {
        id: 8,
        imageUrl: '/red-wine.jpg',
        label: 'Wine',
      }];
    },
    keepDrinking() {
      return [{
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

.hero {
  position: relative;
  color: #fff;
  overflow-y: hidden;
  nav, .content {
    padding: 18px 48px;
  }
  nav {
    background-color: hsla(0, 0%, 0%, 0.2);
    font-size: 16px;
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-between;
    .primary-navigation {
      display: flex;
      align-items: center;
      .navigation-links {
        display: inline;
        li {
          display: inline-block;
          margin-right: 18px;
          &.active {
            font-weight: 700;
          }
        }
      }
    }
    .secondary-navigation {
      display: flex;
      align-items: center;
      .user-logo {
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: #3691a1; // Sika green
        font-weight: 700;
        font-size: 18px;
        width: 36px;
        height: 36px;
        border-radius: 50%;
      }
    }
  }
  .content {
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
    .controls {
      li {
        display: inline;
        margin-right: 12px;
      }
      button {
        border-radius: 4px;
        border: none;
        padding: 12px 32px;
        font-weight: 700;
        font-size: 22px;
        span {
          display: inline-block;
          margin-left: 20px;
        }
      }
    }
  }
}
main {
  padding: 18px 48px;
  margin-top: -72px;
}
</style>
