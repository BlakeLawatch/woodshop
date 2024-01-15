<template>
  <div class="container-fluid">
    <section class="row align-items-end">
      <div class=" col-12 bg-image text-light">
        <Navbar />
        <div class="d-flex justify-content-center">
          <div class="col-12">
            <CarouselComponent />

          </div>
        </div>
      </div>


    </section>

  </div>
</template>

<script>
import CarouselComponent from '../components/CarouselComponent.vue';
import Navbar from '../components/Navbar.vue';

export default {
  setup() {
    return {};
  },
  components: { CarouselComponent, Navbar }
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
