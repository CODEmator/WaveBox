<script setup>
import IconHome from './icons/IconHome.vue'
import IconFacebook from './icons/IconFacebook.vue'
import IconTwitter from './icons/IconTwitter.vue'
import IconInstagram from './icons/IconInstagram.vue'
</script>

<template>
    <footer>
      <div class="footerTop">
        <nav>
          <RouterLink to="/">
            <IconHome/>
          </RouterLink>
          <RouterLink class="menu" to="">About</RouterLink>
          <RouterLink class="menu" to="">Contact</RouterLink>
        </nav>
        <div class="right">
          <IconFacebook/>
          <IconInstagram/>
          <IconTwitter/>
        </div>
      </div>
      <div class="footerBottom">
        <p>
          Copyright &copy; 2022 by WaveBox.<span>All Rights Reserved</span>.
        </p>
      </div>
    </footer>
</template>

<style scoped>
  footer {
    display: flex;
    flex-direction: column;
    /* position: fixed; */
    min-width: 100vw;
    background-color: var(--vt-c-black-soft);
    margin: 1rem 0;
    padding: 1rem;
    bottom: -12vh;
    left: -2rem;
    align-items: center;
    justify-content: space-between;
  }

  nav {
    display: flex;
    color: var(--vt-c-text-dark-2);
    justify-content: space-between;
    align-items: center;
    font-size: 1.3rem;
    gap: 20vw;
  }

  .right {
    display: flex;
    align-items: center;
    justify-items: center;
    gap: 20px;
    margin-left: 25vw;
  }

  /* .menu {
    margin-top: -.3rem;
    font-size: 1.2rem;
  } */

  .footerBottom {
    display: flex;
    place-items: center;
    place-content: center;
    color: var(--vt-c-text-dark-2);
    margin-top: .8rem;
  }

  p {
    color: var(--vt-c-text-dark-2);
    text-align: center;
  }

  @media (hover: hover) {
    a:hover {
      color: var(--vt-c-blue-mute);
    }
  }

@media (min-width: 1024px) {
  footer {
    position: fixed;
    left: 0;
    bottom: -3vh;
  }

  .footerTop {
    display: grid;
    grid-template-columns: 45vw 45vw;
    align-items: center;
    justify-content: space-between;
  }

  nav {
    align-items: flex-start;
    justify-content: left;
    gap: 2rem;
  }

  .right {
    align-items: flex-end;
    justify-content: right;
    gap: 2rem;
  }

  p {
    font-size: 1.2rem;
  }
}
</style>