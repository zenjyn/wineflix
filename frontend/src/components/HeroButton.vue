<template>
  <button :class="btnClass">
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
    btnClass: String,
    faIcon: String,
    label: String,
  },
};
</script>
