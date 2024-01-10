<template>
  <div class="container-fluid">
    <section class="row">
      <div class="bg-image text-light">
        <div class="card elevation-5">
          <marquee scrollamount="15">
            <span>
              <img class="img-fluid max-height" src="src/assets/img/Project-images/couch-table.png" alt="">
              <img class="img-fluid max-height" src="src/assets/img/Project-images/doggy-door.png" alt="">
              <img class="img-fluid max-height" src="src/assets/img/Project-images/corn-hole.png" alt="">
              <img class="img-fluid max-height" src="src/assets/img/Project-images/Shoe-rack.png" alt="">
              <img class="img-fluid max-height" src="src/assets/img/Project-images/board-epoxy.png" alt="">
            </span>
          </marquee>
        </div>
      </div>

    </section>

  </div>
</template>

<script>
export default {
  setup() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
.bg-image {
  background-image: url(src/assets/img/Project-images/bg-image.png);
  height: 100svh;
  background-position: right;
  background-size: cover;
}

.max-height {
  max-height: 50vh;
  height: 50vh;
  width: 60vh;
}

.img-fluid {
  margin-right: 25px;
}

img {
  border-radius: 25px;
}

.card {
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  transform: translateY(-50%);
  padding: 20px;
  border-radius: 15px;
  background: rgba(31, 31, 31, 0);
  border-radius: 16px;
  // box-shadow: 0 4px 30px rgba(0, 0, 0, 0);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(2px);
  // border: 1px solid rgba(31, 31, 31, 0.3);
  // -webkit-mask-image: -webkit-gradient(linear, left 90%, left bottom, from(rgba(0, 0, 0, 1)), to(rgba(0, 0, 0, 0)));
  -webkit-mask-image: linear-gradient(to left, rgba(0, 0, 0, 0), rgb(0, 0, 0), rgba(0, 0, 0, 0));
  // -webkit-mask-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 1));
}
</style>
