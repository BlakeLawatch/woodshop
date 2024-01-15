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
        <div class="dropdown">
          <button class="btn" data-bs-toggle="dropdown" aria-expanded="false">
            <i class="mdi mdi-dots-grid text-light dropdown-options"></i>
          </button>
          <ul class="dropdown-menu drop-menu">
            <li>
              <router-link :to="{ name: 'Gallery' }"
                class="btn text-hover fs-5 fw-bold lighten-30 selectable text-uppercase">
                Gallery
              </router-link>
            </li>

            <li>
              <router-link :to="{ name: 'About' }" class="btn fs-5 fw-bold lighten-30 selectable text-uppercase">
                About
              </router-link>
            </li>
            <li>
              <router-link :to="{ name: 'Contact' }" class="btn fs-5 fw-bold lighten-30 selectable text-uppercase">
                Contact
              </router-link>
            </li>
          </ul>
        </div>







      </ul>
      <!-- LOGIN COMPONENT HERE -->
      <!-- <div>
        <button class="btn text-light" @click="toggleTheme"><i class="mdi"
            :class="theme == 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"></i></button>
      </div>
      <Login /> -->
    </div>
  </nav>
</template>

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

    return {
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

.navbar-color {
  background-color: #113736;
  /* background-color: #CACAAA; */

}

.logo {
  height: 11vh;
  width: auto;
}

.dropdown-options {
  font-size: 8vh;
  border-color: black;
}


.drop-menu {
  background-color: #e4a960;
  border: .5rem solid #361112;
  border-radius: 40px;
  text-align: center;
}
</style>
