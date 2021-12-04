<template>
  <div class="social-networks">
    <SocialLink
      to="https://github.com"
      icon="github.svg"
      alt="Github"
      target="_blank"
    />
    <SocialLink
      to="https://twitter.com"
      icon="twitter.svg"
      alt="Twiiter"
      target="_blank"
    />
    <SocialLink
      to="https://facebook.com"
      icon="facebook.svg"
      alt="Facebook"
      target="_blank"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { SocialLink } from '@/components/atoms';

export default defineComponent({
  components: {
    SocialLink
  }
});
</script>

<style lang="scss" scoped>
.social-networks {
  display: grid;
  grid-gap: 1rem;
}
</style>
