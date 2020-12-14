<template>
  <header class="hero">
    <img class="hero-image" src="/wine-hero.webp">
    <nav class="navigation">
      <section class="primary-navigation">
        <h1>WineFlix</h1>
        <ul class="navigation-links">
          <li class="active">
            <a href="#">Home</a>
          </li>
          <li>
            <a href="#">Whites</a>
          </li>
          <li><a href="#">Reds</a>
          </li>
          <li><a href="#">Blends</a></li>
        </ul>
      </section>
      <section class="secondary-navigation">
        <span class="user-avatar">
          <a href="#">S</a>
        </span>
      </section>
    </nav>
    <div class="hero-content">
      <h2>
        <img alt="Rex Goliath" src="/rex-goliath-logo.png">
      </h2>
      <h3>His Royal Majesty is back.</h3>
      <p>
        America's most unhinged rooster is out of retirement, and this time? He's mad
        as hell.  Experience the unapologetic flavor burst of Rex Goliath.
      </p>
      <ul class="controls">
        <li>
          <button class="primary-action">
            <FontAwesomeIcon icon="play" />
            <span>Drink</span>
          </button>
        </li>
        <li>
          <button class="secondary-action">
            <FontAwesomeIcon icon="info-circle" />
            <span>More Info</span>
          </button>
        </li>
      </ul>
    </div>
  </header>
  <main>
    <ListSection v-bind:title="'Drink Again'">
      <ul>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <span class="new-badge">New!</span>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <span class="new-badge">New!</span>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <span class="new-badge">New!</span>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
          </div>
        </li>
      </ul>
    </ListSection>
    <ListSection v-bind:title="'Keep Drinking'">
      <ul>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
        <li>
          <div class="wine">
            <img src="/red-wine.jpg" alt="Wine">
            <div class="amount-consumed">
              <progress min="0" max="100" value="22"></progress>
            </div>
          </div>
        </li>
      </ul>
    </ListSection>
  </main>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import ListSection from '@/components/ListSection.vue';

export default {
  name: 'App',
  components: {
    FontAwesomeIcon,
    ListSection,
  },
};
</script>

<style lang="scss">
</style>
