<template>
  <div class="services">
    <Service
      v-for="service in services"
      :key="service.title"
      :title="service.title"
      :description="service.description"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { Service } from '@/components/molecules';

export default defineComponent({
  data() {
    return {
      services: [
        {
          title: 'Texto qualquer',
          description:
            'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque ratione sit dicta voluptatem, amet quae quia facere mollitia libero, magni aspernatur cum praesentium labore fugiat pariatur? Qui doloremque eveniet nemo.'
        },
        {
          title: 'Texto qualquer',
          description:
            'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque ratione sit dicta voluptatem, amet quae quia facere mollitia libero, magni aspernatur cum praesentium labore fugiat pariatur? Qui doloremque eveniet nemo.'
        },
        {
          title: 'Texto qualquer',
          description:
            'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Itaque ratione sit dicta voluptatem, amet quae quia facere mollitia libero, magni aspernatur cum praesentium labore fugiat pariatur? Qui doloremque eveniet nemo.'
        }
      ]
    };
  },
  components: {
    Service
  }
});
</script>

<style lang="scss" scoped>
.services {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 5rem;
}
</style>
