<template>
  <ul>
    <li
      v-for="wine in wines"
      :key="wine.id"
    >
      <WineListItem :wine="wine" />
    </li>
  </ul>
</template>

<script>
import WineListItem from '@/components/WineListItem.vue';

export default {
  name: 'WineList',
  components: {
    WineListItem,
  },
  props: {
    wines: Array,
  },
};
</script>
