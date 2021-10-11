<template>
  <div id="app">
    <Cabecalho/>
    <Interativo/>
  </div>
</template>

<script>
import Cabecalho from "./components/header/Cabecalho.vue"
import Interativo from "./components/interativo/Interativo.vue"

export default {
  components: {
    Cabecalho,
    Interativo
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Alata&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300&display=swap');

  html, body {
    margin: 0px;
    width: 1440px;
    font-size: 15px;
    font-family: 'Alata', sans-serif;
  }

  * {
    box-sizing: border-box;
  }
</style>
