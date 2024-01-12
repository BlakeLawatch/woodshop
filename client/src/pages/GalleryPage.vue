<template>
  <div class="gallery">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12 d-flex flex-wrap justify-content-center">
          <div class="col-md-3 p-3" v-for="(image, index) in images" :key="index">
            <img class="img-fluid max-height selectable" :src="image.src" :alt="image.alt" @click="enlargeImage(index)" />
          </div>
        </div>
      </div>
    </div>

    <div v-if="enlargedImageIndex !== -1" class="enlarged" @click="enlargeImage(-1)">
      <img :src="images[enlargedImageIndex].src" :alt="images[enlargedImageIndex].alt" />
    </div>
  </div>

  <audio ref="audioPlayer" :src="audioSrc"></audio>
</template>

<script>
export default {
  data() {
    return {
      enlargedImageIndex: -1,
      images: [
        { src: "src/assets/img/Project-images/bench.png", alt: "Image 1" },
        { src: "src/assets/img/Project-images/board-epoxy.png", alt: "Image 2" },
        { src: "src/assets/img/Project-images/book-rack.png", alt: "Image 3" },
        { src: "src/assets/img/Project-images/corn-hole.png", alt: "Image 4" },
        { src: "src/assets/img/Project-images/couch-table-solo.png", alt: "Image 5" },
        { src: "src/assets/img/Project-images/cutting-board.png", alt: "Image 6" },
        { src: "src/assets/img/Project-images/doggy-door.png", alt: "Image 7" },
        { src: "src/assets/img/Project-images/gardening-tables.png", alt: "Image 8" },
        { src: "src/assets/img/Project-images/picture-frame.png", alt: "Image 9" },
        { src: "src/assets/img/Project-images/Shoe-rack-naked.png", alt: "Image 10" },
        { src: "src/assets/img/Project-images/yello-table-flowers.png", alt: "Image 11" },
        { src: "src/assets/img/Project-images/corn-hole-close.png", alt: "Image 12" },
      ],
    };
  },
  methods: {
    enlargeImage(index) {
      this.enlargedImageIndex = index;
      if (index === 9) {
        import('../assets/audio/FreddyD.mp3').then(module => {
          const sound = module.default || module;
          const audio = new Audio(sound);
          audio.play();
        });
      }
    },
  },
};
</script>

<style scoped lang="scss">
.max-height {
  max-height: 50vh;
  max-width: 50vh;
  height: 50vh;
  width: 100%;
  margin-right: 25px;
  filter: drop-shadow(1rem 1rem 10px rgba(255, 255, 255, 0.23));
  transition: transform 0.3s ease-in-out;
}

.max-height:hover {
  transform: scale(1.1);
}

.enlarged {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.604);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
}

.enlarged img {
  max-width: 90%;
  max-height: 90%;

}

.img-fluid {
  border-radius: 15px;
}

.img-fluid:hover {
  margin-right: 25px;
  filter: drop-shadow(1rem 1rem 10px rgba(0, 0, 0, 0.641));
}

.gallery {
  overflow-x: hidden;
  overflow-y: hidden;
  background-color: #816E5E;
}
</style>



