<template>
  <ul>
    <WineListItem
      v-for="wine in wines"
      :wine="wine"
      :key="wine.id"
    />
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
