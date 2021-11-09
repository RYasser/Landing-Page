<template>
  <div class="card">
    <img v-if="tamanhoTela > 375" class="imgCard" :src="require(`../../assets/images/desktop/${urlImagem}.jpg`)">
    <img v-else class="imgCard imgMobile" :src="require(`../../assets/images/mobile/${urlImagem}.jpg`)">
    <slot/>
  </div>
</template>

<script>
export default {
  props: {
    urlImagem: String,
  },
  data() {
    return {
      tamanhoTela: window.screen.width
    }
  }
}
</script>

<style>
  .card {
    position: relative;
    margin-top: 3.5em;
    overflow: hidden;
  }

  .imgCard {
    filter: brightness(60%);
  }

  .tituloCard {
    position: absolute;
    color: hsl(0, 0%, 100%);
    font-family: Josefin Sans;
    font-size: 2.2em;
    top: 9.6em;
    left: 1.4em;
  }

  @media (max-width: 375px) {
    .tituloCard {
      top: 3em;
      left: 0.6em;
      font-size: 1.2em;
    }

    .imgMobile {
      width: 100%;

    }
  }
  
</style>