<template>
  <div class="container-fluid">
    <section class="row">
      <div class=" col-12 bg-image text-light">
        <Navbar />
        <div class="d-flex justify-content-center">
          <div class="col-12">
            <CarouselComponent />
          </div>
        </div>
      </div>
    </section>
    <section class="row">
      <div class="col-12 bg-card">
        <h1 class="why-us mt-4 ms-4">Why Chose Us?</h1>
        <section class="d-flex justify-content-around">
          <div class="col-3 cards my-5 d-flex flex-column justify-content-center">
            <h1 class="mb-5">1</h1>
            <h2 class="fw-bold">Locally Owned</h2>
          </div>
          <div class="col-3 cards my-5 d-flex flex-column justify-content-center">
            <h1 class="mb-5">2</h1>
            <h2>Locally Sourced Lumber</h2>
          </div>
          <div class="col-3 cards my-5 d-flex flex-column justify-content-center">
            <h1 class="mb-5">3</h1>
            <h2>Born and Raised in Boise ID</h2>
          </div>

        </section>
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
@import url('https://fonts.googleapis.com/css2?family=Black+Ops+One&family=Holtwood+One+SC&family=Martian+Mono:wght@700&family=Permanent+Marker&family=Skranji&display=swap');

.bg-image {
  background-image: url(src/assets/img/Project-images/bg-image.png);
  height: 100svh;
  background-position: right;
  background-size: cover;
}

.bg-card {
  background-color: #361112;
}

.why-us {
  font-family: 'Holtwood One SC', sans-serif;
  color: whitesmoke;
}

.cards {
  height: 30vh;
  color: white;
  background-color: #e4a960;
  border-radius: 15px;
  padding-top: .5rem;
  align-items: center;
}

.cards:hover {
  background-color: #bfa17c;
  transition: ease-in-out 1s;
  animation-name: card;
  animation-duration: 5s;
  // animation-delay: ;

}

@keyframes card {
  from {
    // transform: scaleX(100%);
    transform: scaleY(100%);

  }

  50% {
    // transform: scaleX(120%);
    transform: scaleY(120%);
  }

  to {
    // transform: scaleX(100%);
    transform: scaleY(100%);
  }
}
</style>
