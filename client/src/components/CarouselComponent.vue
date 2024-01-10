<template>
    <div ref="carousel" @wheel.prevent="handleMouseWheel">
        <input type="radio" name="position" :checked="currentPosition === 1" />
        <input type="radio" name="position" :checked="currentPosition === 2" />
        <input type="radio" name="position" :checked="currentPosition === 3" />
        <input type="radio" name="position" :checked="currentPosition === 4" />
        <input type="radio" name="position" :checked="currentPosition === 5" />
        <main id="carousel" class="carousel-container">
            <img class="item img-fluid" src="src/assets/img/Project-images/cutting-boards.png" alt="1">
            <img class="item img-fluid" src="src/assets/img/Project-images/Shoe-rack-naked.png" alt="2">
            <img class="item img-fluid" src="src/assets/img/Project-images/book-rack.png" alt="3">
            <img class="item img-fluid" src="src/assets/img/Project-images/board-epoxy.png" alt="4">
            <img class="item img-fluid" src="src/assets/img/Project-images/corn-hole.png" alt="5">
        </main>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            currentPosition: 1,
            autoScrollInterval: null,
            isScrolling: false,
        };
    },
    methods: {
        autoScroll() {
            this.autoScrollInterval = setInterval(() => {
                this.currentPosition = (this.currentPosition % 5) + 1;
            }, 3000);
        },
        handleMouseWheel(event) {
            clearInterval(this.autoScrollInterval);
            if (event.deltaY > 0) {
                this.currentPosition = (this.currentPosition % 5) + 1;
            } else {
                this.currentPosition = this.currentPosition === 1 ? 5 : this.currentPosition - 1;
            }
            this.isScrolling = true;
        },
        handleMouseWheelEnd() {
            if (this.isScrolling) {
                this.isScrolling = false;
                this.autoScroll();
            }
        },
    },
    mounted() {
        this.autoScroll();
        this.$refs.carousel.addEventListener('wheel', this.handleMouseWheelEnd);
    },
    beforeDestroy() {
        this.$refs.carousel.removeEventListener('wheel', this.handleMouseWheelEnd);
    },
};
</script>
  
  
<style scoped lang="scss">
div {
    // height: 600px;
    margin: 0;
    display: grid;
    grid-template-rows: 500px 100px;
    grid-template-columns: 1fr 30px 30px 30px 30px 30px 1fr;
    align-items: center;
    justify-items: center;
    margin: 0;
    padding: 0;
    background-color: #18181880;
    // width: 30vw;
    // height: 100svh;
    // background-position: cover;
    // background-size: cover;
    overflow: hidden;
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
    transform: rotateY(calc(-10deg * var(--r))) translateX(calc(-350px * var(--r)));
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