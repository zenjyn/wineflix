<template>
  <li>
    <div class="wine">
      <img src="/red-wine.jpg" alt="Wine">
      <span v-if="wine.isNew" class="new-badge">New!</span>
      <div v-if="wine.consumption" class="amount-consumed">
        <progress min="0" max="100" v-bind:value="wine.consumption"></progress>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  name: 'WineListItem',
  props: {
    wine: Object,
  },
};
</script>
