<template>
  <div class="menuToggle">
    <div class="topoMenu">
      <img class="logo" src="../../assets/images/logo.svg">
      <!-- Ativa o evento de click atribuindo um valor booleano armazenado no App -->
      <img @click="desativarMenuMobile" class="fechar" src="../../assets/images/icon-close.svg">
    </div>

    <Menu class="menuMobile"/>
  </div>
</template>

<script>
  import Menu from "../header/Menu.vue"

  export default {
    components: {
      Menu
    },
    methods: {
      desativarMenuMobile() {
        this.$emit('desativarMenuMobile', true)
      }
    }
  }
</script>

<style scoped>
  .menuToggle {
    width: 100%;
    height: 100vh;
    background-color: black;
    padding: 5%;
  }

  .topoMenu {
    margin-bottom: 40%;
    padding: 3%;
  }

  .logo {
    width: 45%;
    float: left;
  }

  .fechar {
    float: right;
  }

  .menuMobile {
    float: none;
    text-transform: uppercase;
    font-size: 1.7em;
    font-family: Josefin Sans;
  }
</style>