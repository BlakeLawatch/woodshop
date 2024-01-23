<template>
  <div class="container-fluid">
    <section class="row">
      <div class=" col-12 bg-image text-light">
        <Navbar />
        <div class="d-flex justify-content-center">
          <div class="col-10 text-center">
            <p class="gradient-text">Knotty Wood Shop</p>
            <div>
              <CarouselComponent class="carousel-view" />
              <SlideshowComponent class="slideshow-view" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="row bg-card">
      <h1 class="why-us mt-4 px-5">Why Choose Us?</h1>
      <section class="text-center">
        <div class="row d-flex justify-content-around">
          <div class="col-11 col-md-3 text-center cards d-flex flex-column justify-content-center">
            <h1 class="mb-5">1</h1>
            <h2 class="fw-bold">Locally Owned</h2>
          </div>
          <div class="col-11 col-md-3 text-center cards d-flex flex-column justify-content-center">
            <h1 class="mb-5">2</h1>
            <h2 class="fw-bold">Locally Sourced Lumber</h2>
          </div>
          <div class="col-11 col-md-3 text-center cards d-flex flex-column justify-content-center">
            <h1 class="mb-5">3</h1>
            <h2 class="fw-bold">Born and Raised in Boise ID</h2>
          </div>
        </div>
      </section>
    </section>
    <section class="row">
      <GalleryComponent />
      <AboutUsComponent />
    </section>
    <section class="row">
    </section>
  </div>
</template>

<script>
import AboutUsComponent from '../components/AboutUsComponent.vue';
import CarouselComponent from '../components/CarouselComponent.vue';
import GalleryComponent from '../components/GalleryComponent.vue';
import Navbar from '../components/Navbar.vue';
import SlideshowComponent from "../components/SlideshowComponent.vue";


export default {
  setup() {
    return {}
      ;
  },
  components: { CarouselComponent, Navbar, SlideshowComponent, GalleryComponent, AboutUsComponent }
}
</script>

<style scoped lang="scss">
.bg-image {
  background-color: #816E5E;
  height: 90svh;
}

.bg-card {
  background-color: #361112;
}



.cards {
  height: 30vh;
  color: #361112c7;
  background-color: #e4a960;
  border-radius: 15px;
  padding-top: .5rem;
  margin-top: 2rem;
  margin-bottom: 5rem;
  align-items: center;
}

.cards:hover {
  background-color: #624120;
  color: #e4a960;
  transition: ease-in-out 1s;
  animation-name: card;
  animation-duration: 1.5s;
  // animation-delay: ;

}

@media(max-width: 767px) {
  .cards {
    margin-bottom: 1rem;
  }
}

@keyframes card {
  from {
    transform: scaleY(100%);

  }

  50% {
    transform: scaleY(110%);
  }

  to {
    transform: scaleY(100%);
  }
}

.gradient-text {
  font-family: "El Messiri", sans-serif;
  font-size: 3.5rem;
  background-image: linear-gradient(to right, #361112, #e4a960, #ddbf99);
  background-size: 100%;
  background-repeat: repeat;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-background-clip: text;
  -moz-text-fill-color: transparent;
}

@media (max-width: 767px) {
  .slideshow-view {
    visibility: hidden;
    display: none;

  }
}

.carousel-view {
  height: 30vh;
  width: 80vw;
}

@media (min-width: 767px) {
  .carousel-view {
    visibility: hidden;
    display: none;
  }
}
</style>
