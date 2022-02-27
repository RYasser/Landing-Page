<template>
  <section class="interativo">
    <div class="containerInterativo">
      <Conteudo/>
    </div>
  </section>
</template>

<script>
import Conteudo from "./Conteudo.vue"

export default {
  components: {
    Conteudo
  }
}
//78
</script>

<style scoped>
  .containerInterativo {
    padding: 9rem;
    width: 60em;
    position: relative;
  }

  @media (max-width: 660px) {
    .containerInterativo {
      padding: 6em 0em 6em 2.5em;
      width: 18em;
    }
  }
</style>