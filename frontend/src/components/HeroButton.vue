<template>
  <button :class="buttonClass">
    <FontAwesomeIcon :icon="faIcon" />
    <span>{{ label }}</span>
  </button>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
  name: 'HeroContent',
  components: {
    FontAwesomeIcon,
  },
  props: {
    buttonClass: String,
    faIcon: String,
    label: String,
  },
};
</script>
