<template>
  <footer class="footer">
    <div class="containerFooter">
      <!-- LOGO -->
      <img class="logo" src="../../assets/images/logo.svg">

      <!-- MENU DA LANDINGPAGE -->
      <Menu class="menu"/>

      <div class="redesSociais">
        <!-- ICONES DAS REDES SOCIAIS -->
        <img src="../../assets/images/icon-facebook.svg">
        <img src="../../assets/images/icon-twitter.svg">
        <img src="../../assets/images/icon-pinterest.svg">
        <img src="../../assets/images/icon-instagram.svg">
      </div>
      <p class="direitosReservados">© 2021 Loopstudios. All rights reserved.</p>
    </div>
  </footer>
</template>

<script>
import Menu from "../header/Menu.vue"

export default {
  components: {
    Menu
  }
}
</script>

<style scoped>
  .footer {
    height: auto;
    width: auto;
  }

  .containerFooter {
    width: auto;
    height: 11em;
    background-color: black;
    padding: 3em 15em 3em 8.5em;
    overflow: hidden;
  }

  .logo {
    position: relative;
    left: 1rem;
    width: 10em;
  }

  .menu {
    position: relative;
    right: 49.5%;
    top: 45%;
  }

  .direitosReservados {
    position: relative;
    left: 75%;
    bottom: 1rem;
    color: hsl(0, 0%, 41%);
    max-width: 18.5rem;
  }

  .redesSociais {
    position: relative;
    left: 86%;
    bottom: 15%;
    display: flex;
    justify-content: space-between;
    max-width: 10rem;
  }
</style>