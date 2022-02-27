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
    padding: 3em 6.8em 3em 6.5em;
    overflow: hidden;
  }

  .logo {
    position: relative;
    left: 1rem;
    width: 10em;
  }

  .menu {
    float: right;
    position: relative;
    right: 63%;
    top: 45%;
    font-size: 15px;
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

  @media (max-width: 460px) {
    .menu  {
      margin: 1.5rem 0rem 1.5rem 0rem;
      position: relative;
      left: 36%;
    }

    .logo {
      left: 2em;
    }

    .containerFooter {
      height: 40%;
      display: flex;
      width: 100%;
      flex-direction: column;
    }

    .iconeRedes {
      margin-left: 5%;
    }

    .redesSociais {
      width: 50rem;
      left: 2rem;
    }

    .direitosReservados {
      width: 50rem;
      left: -300%;
      margin-top: 2rem;
    }
  }
</style>