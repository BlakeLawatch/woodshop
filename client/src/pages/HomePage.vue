<template>
  <div class="container-fluid">
    <section class="row">
      <div class="bg-image text-light">
        <div class="card elevation-5">
          <marquee scrollamount="12">
            <span>
              <img class="img-fluid max-height elevation-5"
                src="https://plus.unsplash.com/premium_photo-1674852890119-fd9f51950ce5?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt="">
              <img class="img-fluid max-height elevation-5"
                src="https://images.unsplash.com/photo-1569695145335-ed8e60d92945?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt="">
              <img class="img-fluid max-height elevation-5"
                src="https://images.unsplash.com/photo-1599651993975-30a482e26467?q=80&w=1887&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt="">
              <img class="img-fluid max-height elevation-5"
                src="https://plus.unsplash.com/premium_photo-1674852890869-045efbe8c54b?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt="">
              <img class="img-fluid max-height elevation-5"
                src="https://images.unsplash.com/photo-1516972810927-80185027ca84?q=80&w=1964&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt="">
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
  background-image: url(https://images.unsplash.com/photo-1547609434-b732edfee020?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8N3x8d29vZCUyMHdvcmt8ZW58MHx8MHx8fDA%3D);
  height: 100svh;
  background-position: center;
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
  background: rgba(31, 31, 31, 0.327);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(2px);
  border: 1px solid rgba(31, 31, 31, 0.3);
  // -webkit-mask-image: -webkit-gradient(linear, left 90%, left bottom, from(rgba(0, 0, 0, 1)), to(rgba(0, 0, 0, 0)));
  -webkit-mask-image: linear-gradient(to left, rgba(0, 0, 0, 0), rgb(0, 0, 0), rgba(0, 0, 0, 0));
  // -webkit-mask-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 1));
}
</style>
