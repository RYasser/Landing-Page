<template>
  <div class="card">
    <img class="imgCard" :src="require(`../../assets/images/desktop/${urlImagem}.jpg`)">
    <slot/>
  </div>
</template>

<script>
export default {
  props: {
    urlImagem: String,
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
</style>