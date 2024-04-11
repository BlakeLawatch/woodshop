<template>
  <nav class="navbar navbar-expand-sm p-5">
    <router-link class="navbar-brand d-flex" :to="{ name: 'Home' }">
      <div class="d-flex flex-column align-items-center">
        <img class="logo" alt="logo" src="src/assets/img/Knotty-logo.png" />
      </div>
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText"
      aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarText">
      <ul class="navbar-nav ms-auto">
        <div class="d-flex dropdown">
          <div class="bordering">
            <li @click="goToGallery()" class="btn options fw-bold text-uppercase">
              Gallery
            </li>
          </div>
          <div class="bordering">
            <li @click="goToAbout()" class="btn options fw-bold text-uppercase">
              About
            </li>
          </div>
          <div>
            <li @click="goToAbout()" class="btn options fw-bold text-uppercase">
              Contact
            </li>
          </div>
        </div>
      </ul>
    </div>
  </nav>
</template>
<!-- <li class="bordering">
            <router-link :to="{ name: 'Gallery' }" class="btn options fw-bold text-uppercase">
              Gallery
            </router-link>
          </li>

          <li class="bordering">
            <router-link :to="{ name: 'About' }" class="btn options fw-bold text-uppercase">
              About
            </router-link>
          </li>
          <li>
            <router-link :to="{ name: 'Contact' }" class="btn options fw-bold text-uppercase">
              Contact
            </router-link>
          </li> -->
<!-- LOGIN COMPONENT HERE -->
<!-- <div>
        <button class="btn text-light" @click="toggleTheme"><i class="mdi"
            :class="theme == 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"></i></button>
      </div>
      <Login /> -->

<script>
import { onMounted, ref } from 'vue';
import { loadState, saveState } from '../utils/Store.js';
import Login from './Login.vue';
export default {
  setup() {

    const theme = ref(loadState('theme') || 'light')

    onMounted(() => {
      document.documentElement.setAttribute('data-bs-theme', theme.value)
    })
    function goToGallery() {
      let elem = document.getElementById("Gallery")
      elem?.scrollIntoView({ behavior: 'smooth' })
    }
    function goToAbout() {
      let elem = document.getElementById("About")
      elem?.scrollIntoView({ behavior: 'smooth' })
    }
    // function goToContact() {
    //   window.scrollTo(0, 3000)
    // }

    return {
      goToGallery,
      goToAbout,
      // goToContact,
      theme,
      toggleTheme() {
        theme.value = theme.value == 'light' ? 'dark' : 'light'
        document.documentElement.setAttribute('data-bs-theme', theme.value)
        saveState('theme', theme.value)
      }
    }
  },
  components: { Login }
}
</script>

<style scoped>
a:hover {
  text-decoration: none;
}

.nav-link {
  text-transform: uppercase;
}

.navbar-nav .router-link-exact-active {
  border-bottom: 2px solid var(--bs-success);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

@media screen and (min-width: 768px) {
  nav {
    height: 10svh;
  }
}

.logo {
  height: 11vh;
  width: auto;
  filter: drop-shadow(2px 2px 2px #200606);
}

.bordering {
  border-right: thin dashed #361112;
}

.options {
  font-size: 1.4rem;
  text-shadow: 2px 2px 1.5px #361112;
  color: white;
}

.options:hover {
  text-shadow: 4px 4px 3.5px #361112;
  transition: ease-in-out .4s;
}
</style>
