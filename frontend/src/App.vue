<template>
  <Header :navigationLinks="navigationLinks" />
  <main>
    <ListSection title="Drink Again">
      <WineList v-bind:wines='drinkAgainWines' />
    </ListSection>
    <ListSection title="Keep Drinking">
      <WineList v-bind:wines='keepDrinkingWines' />
    </ListSection>
  </main>
</template>

<script>
import Header from '@/components/Header.vue';
import ListSection from '@/components/ListSection.vue';
import WineList from '@/components/WineList.vue';

export default {
  name: 'App',
  components: {
    Header,
    ListSection,
    WineList,
  },
  computed: {
    navigationLinks() {
      return [
        { url: '#', label: 'Home', isActive: true },
        { url: '#', label: 'Whites', isActive: false },
        { url: '#', label: 'Reds', isActive: false },
        { url: '#', label: 'Blends', isActive: false },
      ];
    },
    drinkAgainWines() {
      return [
        { id: 37, isNew: true, consumption: 0 },
        { id: 38, isNew: false, consumption: 0 },
        { id: 39, isNew: true, consumption: 0 },
        { id: 40, isNew: false, consumption: 0 },
        { id: 41, isNew: true, consumption: 0 },
        { id: 42, isNew: false, consumption: 0 },
        { id: 43, isNew: false, consumption: 0 },
        { id: 44, isNew: false, consumption: 0 },
      ];
    },
    keepDrinkingWines() {
      return [
        { id: 4, isNew: false, consumption: 22 },
        { id: 5, isNew: false, consumption: 22 },
        { id: 6, isNew: false, consumption: 50 },
        { id: 7, isNew: false, consumption: 22 },
        { id: 10, isNew: false, consumption: 22 },
        { id: 22, isNew: false, consumption: 22 },
        { id: 23, isNew: false, consumption: 67 },
        { id: 24, isNew: false, consumption: 22 },
      ];
    },
  },
};
</script>

<style lang="scss">
</style>
