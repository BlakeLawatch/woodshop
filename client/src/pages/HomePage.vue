<template>
  <div class="container-fluid">
    <section class="row align-items-end">
      <div class="bg-image text-light">
        <CarouselComponent />

      </div>

    </section>

  </div>
</template>

<script>
import CarouselComponent from '../components/CarouselComponent.vue';

export default {
  setup() {
    return {};
  },
  components: { CarouselComponent }
}
</script>

<style scoped lang="scss">
.bg-image {
  background-image: url(src/assets/img/Project-images/bg-image.png);
  height: 100svh;
  background-position: right;
  background-size: cover;
}
</style>
