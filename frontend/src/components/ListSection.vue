<template>
  <section class="category">
    <h2>{{title}}</h2>
    <slot></slot>
  </section>
</template>

<script>
export default {
  name: 'ListSection',
  props: {
    title: String,
  },
};
</script>
