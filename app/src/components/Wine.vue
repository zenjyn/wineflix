<template>
  <div class="wine">
    <img src="/red-wine.jpg" alt="Wine" />
    <div class="amount-consumed"><progress min="0" max="100" value="15"></progress></div>
  </div>
</template>

<script>
export default {
  name: 'Wine',
};
</script>

<style lang="scss">
.wine {
  width: 300px;
  margin-right: 4px;
  position: relative;
  img {
    border-radius: 4px;
    height: 205px;
  }
  .new-badge {
    position: absolute;
    right: 0;
    top: 0;
    background-color: hsl(350, 80%, 40%);
    color: #fff;
    font-weight: 700;
    padding: 8px 12px;
  }
  .amount-consumed {
    padding: 0 48px 16px 48px;
    progress {
      width: 100%;
      height: 4px;
      background-color: hsl(0, 0%, 30%);
      border: none;
      &::-webkit-progress-bar, &::-moz-progress-bar {
        background-color: hsl(350, 80%, 40%);
      }
    }
  }
</style>
