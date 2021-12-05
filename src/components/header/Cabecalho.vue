<template>
  <header class="cabecalho">
    <div class="containerCabecalho">
      <img class="logo" src="../../assets/images/logo.svg">
      <Menu class="menu"/>
      <img @click="ativarMenuMobile" class="toggle" src="../../assets/images/icon-hamburger.svg">
      <!--TEXTO DA CAIXA DA TÍTULO PRINCIPAL DO CABEÇALHO-->
      <TituloPrincipal class="tituloPrincipal">
        <h1 class="textoTitulo">IMMERSIVE<br>EXPERIENCES<br>THAT DELIVER</h1>
      </TituloPrincipal>
    </div>
  </header>
</template>

<script>
import TituloPrincipal from "./TituloPrincipal.vue"
import Menu from "./Menu.vue"

export default {
  components: {
    TituloPrincipal,
    Menu
  },
  methods: {
    ativarMenuMobile() {
      this.$emit('ativarMenuMobile', false)
    }
  }
}
</script>

<style scoped>
  .cabecalho {
    background-image: 
      linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
      url('../../assets/images/desktop/image-hero.jpg');
    opacity: 1;
    height: auto;
  }

  .menu {
    float: right;
    font-size: 15px;
  }

  .toggle {
    display: none;
    float: right;
  }

  .logo {
    float: left;
  }

  .containerCabecalho {
    padding: 4rem 6rem;
  }

  .tituloPrincipal {
    margin-top: 160px;
  }

  @media (max-width: 375px) {
    .cabecalho {
      background-image: 
        url('../../assets/images/mobile/image-hero.jpg');
      height: 42rem;
      background-size: 380px;
    }

    .menu {
      display: none;
    }

    .toggle {
      display: block;
    }

    .containerCabecalho {
      padding: 35px 25px;
    }

    .tituloPrincipal {
      width: 100%;
      margin-top: 14rem;
    }

    .logo {
      width: 12em;
    }
  }
</style>