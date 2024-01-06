<template>
  <body>
    <input type="radio" name="position" :checked="currentPosition === 1" />
    <input type="radio" name="position" :checked="currentPosition === 2" />
    <input type="radio" name="position" :checked="currentPosition === 3" />
    <input type="radio" name="position" :checked="currentPosition === 4" />
    <input type="radio" name="position" :checked="currentPosition === 5" />
    <main id="carousel" class="carousel-container">
      <img class="item img-fluid"
        src="https://plus.unsplash.com/premium_photo-1674852890119-fd9f51950ce5?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="1">
      <img class="item img-fluid"
        src="https://images.unsplash.com/photo-1569695145335-ed8e60d92945?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="2">
      <img class="item img-fluid"
        src="https://images.unsplash.com/photo-1599651993975-30a482e26467?q=80&w=1887&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="3">
      <img class="item img-fluid"
        src="https://plus.unsplash.com/premium_photo-1674852890869-045efbe8c54b?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="4">
      <img class="item img-fluid"
        src="https://images.unsplash.com/photo-1516972810927-80185027ca84?q=80&w=1964&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        alt="5">
    </main>
  </body>
</template>

<script>
export default {
  data() {
    return {
      currentPosition: 1,
    };
  },
  setup() {
    return {};
  },
  methods: {
    autoScroll() {
      setInterval(() => {
        this.currentPosition = (this.currentPosition % 5) + 1;
      }, 2000);
    },
  },
  mounted() {
    this.autoScroll();
  },
};
</script>

<style scoped lang="scss">
body {
  height: 600px;
  margin: 0;
  display: grid;
  grid-template-rows: 500px 100px;
  grid-template-columns: 1fr 30px 30px 30px 30px 30px 1fr;
  align-items: center;
  justify-items: center;
  margin: 0;
  padding: 0;
  background-color: #181818;
  height: 100svh;
  background-position: cover;
  background-size: cover;
}

.carousel-container {
  max-width: 100%;
  margin: 0 auto;
}

main#carousel {
  grid-row: 1 / 2;
  grid-column: 1 / 8;
  width: 100vw;
  height: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  transform-style: preserve-3d;
  perspective: 600px;
  --items: 5;
  --middle: 3;
  --position: 1;
  pointer-events: none;
}

img.item {
  max-width: 100%;
  position: absolute;
  width: 300px;
  height: 400px;
  --r: calc(var(--position) - var(--offset));
  --abs: max(calc(var(--r) * -1), var(--r));
  transition: all 0.25s linear;
  transition: transform 1s ease-in-out;
  transform: rotateY(calc(-10deg * var(--r))) translateX(calc(-300px * var(--r)));
  z-index: calc((var(--position) - var(--abs)));
  -webkit-box-reflect: below 0px linear-gradient(to bottom, rgba(0, 0, 0, 0.0), rgba(0, 0, 0, 0.4));
}

img.item:nth-of-type(1) {
  --offset: 1;
}

img.item:nth-of-type(2) {
  --offset: 2;
}

img.item:nth-of-type(3) {
  --offset: 3;
}

img.item:nth-of-type(4) {
  --offset: 4;
}

img.item:nth-of-type(5) {
  --offset: 5;
}

input:nth-of-type(1) {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}

input:nth-of-type(1):checked~main#carousel {
  --position: 1;
}

input:nth-of-type(2) {
  grid-column: 3 / 4;
  grid-row: 2 / 3;
}

input:nth-of-type(2):checked~main#carousel {
  --position: 2;
}

input:nth-of-type(3) {
  grid-column: 4 /5;
  grid-row: 2 / 3;
}

input:nth-of-type(3):checked~main#carousel {
  --position: 3;
}

input:nth-of-type(4) {
  grid-column: 5 / 6;
  grid-row: 2 / 3;
}

input:nth-of-type(4):checked~main#carousel {
  --position: 4;
}

input:nth-of-type(5) {
  grid-column: 6 / 7;
  grid-row: 2 / 3;
}

input:nth-of-type(5):checked~main#carousel {
  --position: 5;
}
</style>
