<template>
  <div class="hero-content">
    <h2>
      <img alt="Rex Goliath" src="/rex-goliath-logo.png">
    </h2>
    <h3>His Royal Majesty is back.</h3>
    <p>
      America's most unhinged rooster is out of retirement, and this time? He's mad
      as hell.  Experience the unapologetic flavor burst of Rex Goliath.
    </p>
    <ul class="controls">
      <li>
        <HeroButton
          btnClass="primary-action"
          faIcon="play"
          label="Drink"
        />
      </li>
      <li>
        <HeroButton
          btnClass="secondary-action"
          faIcon="info-circle"
          label="More Info"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import HeroButton from '@/components/HeroButton.vue';

export default {
  name: 'HeroContent',
  components: {
    HeroButton,
  },
};
</script>
