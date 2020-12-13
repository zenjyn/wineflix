<template>
  <span class="user-avatar"><a :href="linkUrl">{{initial}}</a></span>
</template>

<script>
export default {
  name: 'UserAvatar',
  props: {
    initial: String,
    linkUrl: String,
  },
};
</script>

<style lang="scss">
  .user-avatar {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #3691a1; // Sika green
    font-weight: 700;
    font-size: 18px;
    width: 36px;
    height: 36px;
    border-radius: 50%;
  }
</style>
