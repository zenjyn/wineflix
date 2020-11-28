<template>
  <button class="secondary-action">
    <FontAwesomeIcon :icon="icon" /><span>{{ label }}</span>
  </button>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
  name: 'SecondaryAction',
  components: {
    FontAwesomeIcon,
  },
  props: {
    label: String,
    icon: String,
  },
};
</script>

<style lang="scss">
.secondary-action {
  background-color: hsla(0, 0%, 100%, 0.30);
  color: hsl(0, 0%, 90%);
}
</style>
