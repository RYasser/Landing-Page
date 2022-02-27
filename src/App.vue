<template>
  <div id="app">
    <div v-if="menuToggle" class="containerPadrao">
      <!-- Escuta o evento para ativar o menu mobile -->
      <Cabecalho @ativarMenuMobile="ativarMenuMobile($event)" class="cabecalho"/>
      <Interativo class="interativo"/>
      <Criacoes class="criacoes"/>
      <Footer class="footer"/>
    </div>
    <!-- Escuta o evento para desativar o menu mobile -->
    <MenuMobile @desativarMenuMobile="desativarMenuMobile($event)"  v-else/>
  </div>
</template>

<script>
import Cabecalho from "./components/header/Cabecalho.vue"
import Interativo from "./components/interativo/Interativo.vue"
import Criacoes from "./components/criacoes/Criacoes.vue"
import Footer from "./components/footer/Footer.vue"
import MenuMobile from "./components/menuMobile/menuMobile.vue"

export default {
  components: {
    Cabecalho,
    Interativo,
    Criacoes,
    Footer,
    MenuMobile
  },
  data() {
    return {
      menuToggle: true
    }
  },
  methods: {
    // Pega o valor booleano do evento de click toggle menu de ativar e desativar
    ativarMenuMobile(event) {
      this.menuToggle = event
    },

    desativarMenuMobile(event) {
      this.menuToggle = event
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Alata&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300&display=swap');

  * {
    box-sizing: border-box;
  }

  html, body {
    margin: 0px;
    font-size: 15px;
    width: 100%;
    font-family: 'Alata', sans-serif;
  }

  .cabecalho, .interativo, .criacoes, .footer {
    width: inherit;
  }

  @media (max-width: 660px) {
    html, body {
      height: auto;
    }
  }
</style>
