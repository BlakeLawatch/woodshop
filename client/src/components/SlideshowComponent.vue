<template>
  <div id="carouselExampleFade" class="carousel slide carousel-fade d-flex justify-content-center">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="src/assets/img/Project-images/couch-table-zoom-out.png" alt="...">
      </div>
      <div class="carousel-item">
        <img src="src/assets/img/Project-images/corn-hole-close.png" alt="...">
      </div>
      <div class="carousel-item">
        <img src="src/assets/img/Project-images/Shoe-rack-naked.png" alt="...">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>


<script>
import { AppState } from '../AppState';
import { computed, reactive, onMounted } from 'vue';
export default {
  setup() {
  }
};
</script>


<style lang="scss" scoped>
img {
  height: 50vh;
  width: 50vw;
}
</style>