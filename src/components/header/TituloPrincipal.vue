<template>
  <div class="containerTituloPrincipal">
    <slot/>
  </div>
</template>

<style scoped>
  .containerTituloPrincipal {
    font-family: Josefin Sans;
    border: solid 2px hsl(0, 0%, 100%);
    color: hsl(0, 0%, 90%);
    width: 37rem;
    height: 100%;
    font-size: 1.70rem;
    letter-spacing: 5px;
    padding: 4px 18px;
    overflow: hidden;

  }

  .textoTitulo {
    margin-left: 15px;
  }
</style>