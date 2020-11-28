<template>
  <header class="hero">
    <HeroImage />
    <img class="hero-image" src="/wine1.webp" />
    <nav>
      <section class="primary-navigation">
        <Logo />
        <ul class="navigation-links">
          <li class="active"><a href="#">Home</a></li>
          <li><a href="#">Whites</a></li>
          <li><a href="#">Reds</a></li>
          <li><a href="#">Blends</a></li>
        </ul>
      </section>
      <section class="secondary-navigation">
        <a href="#"><span class="user-logo">S</span></a>
      </section>
    </nav>
    <div class="content">
      <h2><img alt="Rex Goliath" src="/rex-goliath-logo.png" /></h2>
      <h3>His Royal Majesty is back.</h3>
    <p>America's most unhinged rooster is out of retirement, and this time? He's mad as hell.
    Experience the unapologetic flavor burst of Rex Goliath.</p>
    <ul class="controls">
      <li>
        <button class="primary-action">
          <FontAwesomeIcon icon="play" /><span>Drink</span>
        </button>
      </li>
      <li>
        <button class="secondary-action">
          <FontAwesomeIcon icon="info-circle" /><span>More Info</span>
        </button>
      </li>
    </ul>
  </div>
</header>
<main>
  <section class="category">
    <h2>Drink It Again</h2>
    <ul>
      <li>
        <div class="wine">
           <span class="new-badge">New!</span>
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
           <span class="new-badge">New!</span>
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
        </div>
      </li>
    </ul>
  </section>
  <Category :wine="keepDrinking" heading="Keep Drinking" />
</main>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import Logo from './components/Logo.vue';
import HeroImage from './components/HeroImage.vue';
// import Wine from './components/Wine.vue';
import Category from './components/Category.vue';

export default {
  name: 'App',
  components: {
    FontAwesomeIcon,
    Logo,
    HeroImage,
    // Wine,
    Category,
  },
  computed: {
    imageUrl() {
      return '/red-wine.jpg';
    },
    progress() {
      return 22;
    },
    label() {
      return 'Wine';
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
      .primary-action {
        background-color: hsl(0, 0%, 90%);
        color: hsl(0, 0%, 5%);
      }
      .secondary-action {
        background-color: hsla(0, 0%, 100%, 0.30);
        color: hsl(0, 0%, 90%);
      }
    }
  }
}
main {
  padding: 18px 48px;
  margin-top: -72px;
}
</style>
