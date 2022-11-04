<script setup>
import { RouterLink } from 'vue-router'
import JoinBtn from './buttons/JoinNow.vue'
import MenuIcon from './icons/IconMenu.vue'
</script>

<script>
export  default {
  data() {
    return {
      showMobileMenu: false,
    };
  },
  methods: {
    showMenu() {
      this.showMobileMenu = !this.showMobileMenu
    }
  }
}
</script>

<template>
    <header>
        <div class="logowrap">
            <img alt="Wave logo" class="logo" src="@/assets/logo.svg" width="50" height="50" />
            <h1 class="logotext">Wave</h1>
        </div>

        <div class="wrapper">
            <MenuIcon class="menu" v-on:click="showMenu ()"/>

            <div class="nav-content" :class="this.showMobileMenu ? 'open-menu' : 'close-menu'">
                <nav class="hidden">
                <!-- <RouterLink to="/">Home</RouterLink> -->
                <RouterLink to="/discover">Discover</RouterLink>
                <RouterLink to="/login">Login</RouterLink>
                <JoinBtn/>
            </nav>
            </div>
        </div>
    </header>
</template>

<style scoped>
  header {
    display: flex;
    line-height: 1.5;
    justify-content: space-between;
    align-items: center;
    /* position: fixed; */
    /* max-height: 100vh; */
  }

  .logowrap {
    display: flex;
  }

  .logotext {
    font-size: 1.8rem;
    margin-top: .3rem;
    margin-left: .2rem;
  }

  .wrapper {
    display: flex;
    flex-direction: column;
  }

  .nav-content {
    position: fixed;
    display: flex;
    z-index: 999;
    place-items: center;
    top: 10vh;
    right: 0;
    left: 0;
    width: 100vw;
    margin-left: 3rem;
    margin-right: auto;
  }
  .open-menu {
    display: block;
  }
  .close-menu {
  display: none;
  }

  nav {
    display: flex;
    width: 100%;
    font-size: 1.3rem;
    text-align: center;
    margin-top: 2rem;
    align-items: center;
  }

  nav a.router-link-exact-active {
    color: var(--color-text);
  }

  nav a.router-link-exact-active:hover {
    background-color: transparent;
  }

  nav a {
    display: inline-block;
    padding: 0 1rem;
    border-left: 1px solid var(--color-border);
  }

  nav a:first-of-type {
    border: 0;
  }


@media (min-width: 1024px) {
  .menu {
    display: none;
  }


  .logowrap {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .logotext {
    font-size: 2.1rem;
    margin-left: -1.5rem;
  }
  
  .logo {
    display: flex;
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .nav-content {
    position: inherit;
    display: flex;
    z-index: inherit;
    align-items: center;
    top: auto;
    right: auto;
    left: auto;
    width: auto;
}
  
  nav {
    display: flex;
    text-align: left;
    margin-left: -1rem;
    font-size: 1.6rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>



