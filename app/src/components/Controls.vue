<template>
  <ul class="controls">
    <li>
      <PrimaryAction
        label="Drink"
        icon="play"
      />
    </li>
    <li>
      <SecondaryAction
        label="More Info"
        icon="info-circle"
      />
    </li>
  </ul>
</template>

<script>
import PrimaryAction from './PrimaryAction.vue';
import SecondaryAction from './SecondaryAction.vue';

export default {
  name: 'Controls',
  components: {
    PrimaryAction,
    SecondaryAction,
  },
};
</script>

<style lang="scss">
.controls {
  li {
    display: inline;
    margin-right: 12px;
  }
  button {
    border-radius: 4px;
    border: none;
    padding: 12px 32px;
    font-weight: 700;
    font-size: 22px;
    span {
      display: inline-block;
      margin-left: 20px;
    }
  }
}
</style>
