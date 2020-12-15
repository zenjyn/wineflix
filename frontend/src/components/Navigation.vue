<template>
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
</template>

<script>
import NavigationLink from '@/components/NavigationLink.vue';

export default {
  name: 'Navigation',
  components: {
    NavigationLink,
  },
  computed: {
    navigationLinks() {
      return [
        {
          url: '#',
          label: 'Home',
          isActive: true,
        },
        {
          url: '#',
          label: 'Whites',
          isActive: false,
        },
        {
          url: '#',
          label: 'Reds',
          isActive: false,
        },
        {
          url: '#',
          label: 'Blends',
          isActive: false,
        },
      ];
    },
  },
};
</script>
