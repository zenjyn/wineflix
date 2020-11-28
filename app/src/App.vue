<template>
  <header class="hero">
    <Logo />
    <nav>
      <section class="primary-navigation">
        <h1>WineFlix</h1>
        <ul>
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
  <section class="category">
    <h2>Keep Drinking</h2>
    <ul>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="71"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="80"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="15"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="70"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="33"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="2"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="77"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="5"></progress></div>
        </div>
      </li>
      <li>
        <div class="wine">
          <img src="/red-wine.jpg" alt="Wine" />
          <div class="amount-consumed"><progress min="0" max="100" value="43"></progress></div>
        </div>
      </li>
    </ul>
  </section>
</main>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import Logo from './components/Logo.vue';

export default {
  name: 'App',
  components: {
    FontAwesomeIcon,
    Logo,
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
  .hero-image {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: -1;
  }
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
      ul {
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
      .wine {
        width: 300px;
        margin-right: 4px;
        position: relative;
        img {
          border-radius: 4px;
          height: 205px;
        }
        .new-badge {
          position: absolute;
          right: 0;
          top: 0;
          background-color: hsl(350, 80%, 40%);
          color: #fff;
          font-weight: 700;
          padding: 8px 12px;
        }
        .amount-consumed {
          padding: 0 48px 16px 48px;
          progress {
            width: 100%;
            height: 4px;
            background-color: hsl(0, 0%, 30%);
            border: none;
            &::-webkit-progress-bar, &::-moz-progress-bar {
              background-color: hsl(350, 80%, 40%);
            }
          }
        }
      }
    }
  }
}
</style>
