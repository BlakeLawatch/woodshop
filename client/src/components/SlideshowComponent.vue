<template>
  <div id="carouselExampleIndicators" class="carousel slide carousel-fade">
    <div class="carousel-indicators p-4">
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
        aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
        aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
        aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner p-4">
      <div class="carousel-item active">
        <img src="src/assets/img/Project-images/corn-hole.png" class="img-fluid" alt="0">
      </div>
      <div class="carousel-item">
        <img src="src/assets/img/Project-images/book-rack-backside.png" class="img-fluid" alt="1">
      </div>
      <div class="carousel-item">
        <img src="src/assets/img/Project-images/cutting-boards.png" class="img-fluid" alt="2">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
      <span class="font"><i class="mdi mdi-less-than"></i></span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
      <span><i class="mdi mdi-greater-than"></i></span>
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
  width: 45vw;
}

.img-fluid {
  border-radius: 15px;
  margin-right: 25px;
  box-shadow: (1rem 1rem 10px rgba(0, 0, 0, 0.641));

}

.mdi-greater-than {
  font-size: 10rem;
}


.mdi-less-than {
  font-size: 10rem;
}
</style>