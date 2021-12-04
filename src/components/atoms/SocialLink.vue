<template>
  <a class="social-link" :href="to" :target="target">
    <!-- iconPath() => required é necessário pois não estamos definindo o caminho de forma estática mais sim de forma dinâmica -->
    <img :src="iconPath" :alt="alt" />
  </a>
</template>

<script lang="ts">
type target = '_blank' | '_self' | '_parent' | '_top';

import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    to: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      required: true
    },
    alt: {
      type: String,
      required: true
    },
    target: {
      type: String,
      validator: (value: target) => {
        return ['_blank', '_self', '_parent', '_top'].includes(value);
      }
    }
  },
  computed: {
    iconPath() {
      // required é necessário pois não estamos definindo o caminho de forma estática mais sim de forma dinâmica,
      // e no javascript é assim que importamos elementos externos.
      return require(`@/assets/images/icons/${this.icon}`);
    }
  }
});
</script>

<style lang="scss" scoped>
.social-link {
  background-color: #ff895f;
  width: 47px;
  height: 47px;
  border-radius: 5rem;
  display: grid;
  justify-items: center;
  align-items: center;
  transition: transform 0.2s linear;
  &:hover {
    transform: scale(1.1);
  }
  img {
    width: 23px;
    height: 23px;
  }
}
</style>
