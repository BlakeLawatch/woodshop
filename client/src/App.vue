<template>
  <!-- <header>
    <Navbar />
  </header> -->
  <main>
    <router-view />
  </main>
</template>

<script>
import { computed } from 'vue'
import { AppState } from './AppState'
import Navbar from './components/Navbar.vue'



export default {
  setup() {
    return {
      appState: computed(() => AppState)
    }
  },
  components: { Navbar }
}
</script>
<style lang="scss">
@import "./assets/scss/main.scss";
@import url('https://fonts.googleapis.com/css2?family=Black+Ops+One&family=Holtwood+One+SC&family=Martian+Mono:wght@700&family=Permanent+Marker&family=Skranji&display=swap');
@import url('https://fonts.googleapis.com/css2?family=El+Messiri:wght@400..700&display=swap');




:root {
  --main-height: calc(100vh - 32px - 64px);
}

footer {
  display: grid;
  place-content: center;
  height: 32px;
}

.why-us {
  font-family: 'Holtwood One SC', sans-serif;
  color: whitesmoke;
}

.bg-card {
  background-color: #361112;
}
</style>
