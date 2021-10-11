<template>
  <header class="cabecalho">
    <div class="containerCabecalho">
      <Menu/>
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
  }
}
</script>

<style scoped>
  .cabecalho {
    background-image: 
      linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
      url('../assets/images/desktop/image-hero.jpg');
    opacity: 1;
    height: 600px; 
  }

  .containerCabecalho {
    padding: 70px 120px;
  }

  .tituloPrincipal {
    margin-top: 160px;
  }
</style>