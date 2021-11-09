<template>
  <footer class="footer">
    <div class="containerFooter">
      <!-- LOGO -->
      <img class="logo" src="../../assets/images/logo.svg">

      <!-- MENU DA LANDINGPAGE -->
      <Menu class="menu"/>

      <div class="redesSociais">
        <!-- ICONES DAS REDES SOCIAIS -->
        <img class="iconeRedes" src="../../assets/images/icon-facebook.svg">
        <img class="iconeRedes" src="../../assets/images/icon-twitter.svg">
        <img class="iconeRedes" src="../../assets/images/icon-pinterest.svg">
        <img class="iconeRedes" src="../../assets/images/icon-instagram.svg">
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

  @media (max-width: 375px) {
    .containerFooter {
      height: 40%;
      display: flex;
      width: 30em;
      flex-direction: column;
    }

    .iconeRedes {
      margin-left: 5%;
    }

    .redesSociais {
      width: 50rem;
      left: 10%;
    }

    .direitosReservados {
      width: 50rem;
      left: -50%;
      margin-top: 2rem;
    }
  }
</style>