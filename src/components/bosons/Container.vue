<template>
  <div class="container">
    <!-- Para que seja possível reutilizar o componente é necessário que o mesmo possua algum elemento, por isso que adicionamos um slot. -->
    <slot />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({});
</script>

<style lang="scss" scoped>
.container {
  width: 85%;
  max-width: 1150px;
  margin: 0 auto;
}
</style>
