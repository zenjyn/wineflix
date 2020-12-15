<template>
  <span class="user-avatar">
    <a :href="link">{{ label }}</a>
  </span>
</template>

<script>
export default {
  name: 'UserAvatar',
  props: {
    link: String,
    label: String,
  },
};
</script>
