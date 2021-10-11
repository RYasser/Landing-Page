<template>
  <article class="containerTextoInterativo">
    <slot/>
  </article>
</template>

<style scoped>
  .containerTextoInterativo {
    padding: 4.5em 4.5em 0em 4.5em;
    color: black;
    width: 65%;
    background-color: white;
    font-size: 14.5px;
    font-weight: bold;
    overflow: hidden;
    color: hsl(0, 0%, 55%);
    line-height: 26px;
  }

  h2 {
    font-family: Josefin Sans;
    line-height: 42px;
    color: hsl(0, 0%, 20%);
  }
</style>