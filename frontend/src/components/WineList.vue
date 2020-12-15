<template>
  <ul>
    <WineListItem
      v-for="(wine, index) in wines"
      :wine="wine"
      :key="index"
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
