<template>
  <nav class="navigation">
    <section class="primary-navigation">
      <Logo />
      <NavigationLinks />
    </section>
    <section class="secondary-navigation">
      <UserAvatar initial="S" linkUrl="#" />
    </section>
  </nav>
</template>

<script>
import Logo from './Logo.vue';
import NavigationLinks from './NavigationLinks.vue';
import UserAvatar from './UserAvatar.vue';

export default {
  name: 'Navigation',
  components: {
    Logo,
    NavigationLinks,
    UserAvatar,
  },
};
</script>

<style lang="scss">
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
    }
  }
</style>
