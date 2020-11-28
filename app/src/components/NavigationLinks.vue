<template>
  <ul class="navigation-links">
    <li class="active"><a href="#">Home</a></li>
    <li><a href="#">Whites</a></li>
    <li><a href="#">Reds</a></li>
    <li><a href="#">Blends</a></li>
  </ul>
</template>

<script>
export default {
  name: 'NavigationLinks',
};
</script>

<style lang="scss">
.navigation-links {
  display: inline;
  li {
    display: inline-block;
    margin-right: 18px;
    &.active {
      font-weight: 700;
    }
  }
}
</style>
