<template>
    <nav class="navigation">
      <section class="primary-navigation">
        <h1>WineFlix</h1>
        <ul class="navigation-links">
          <li
            v-for="navigationLink in navigationLinks"
            :key="navigationLink.label"
            :class="{ active: navigationLink.isActive }"
          >
            <NavigationLink
              :url="navigationLink.url"
              :label="navigationLink.label"
            />
          </li>
        </ul>
      </section>
      <section class="secondary-navigation">
        <UserAvatar link="#" label="S" />
      </section>
    </nav>
</template>

<script>
import NavigationLink from '@/components/NavigationLink.vue';
import UserAvatar from '@/components/UserAvatar.vue';

export default {
  name: 'AppNavigation',
  components: {
    NavigationLink,
    UserAvatar,
  },
  props: {
    navigationLinks: Array,
  },
};
</script>
