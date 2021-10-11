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
</script>

<style scoped>
  .containerInterativo {
    padding: 9rem;
    width: 900px;
    position: relative;
  }
</style>