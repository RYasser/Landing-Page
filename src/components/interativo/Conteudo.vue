<template>
  <div class="containerConteudo">
    <!-- ILUSTRAÇÃO DO CONTEÚDO -->
    <img class="imagemInterativo" src="../../assets/images/desktop/image-interactive.jpg">

    <!-- TEXTO SOBRE O CONTEÚDO -->
    <TextoInterativo class="textoInterativo">
      <h2>THE LEADER IN <br> INTERACTIVE VR</h2>
      <p>Founded in 2011, Loopstudios has been producing world-class<br>
      virtual reality projects for some of the best companies around the<br>
      globe. Our award-winning creations have transformed<br>
      businesses through digital expriences that bind to their brand.</p>
    </TextoInterativo>
  </div>
</template>

<script>
import TextoInterativo from "./TextoInterativo.vue"

export default {
  components: {
    TextoInterativo
  }
}
</script>

<style scoped>
  .textoInterativo {
    padding: 6em;
    position: absolute;
    top: 21rem;
    left: 46rem;
  }

  h2 {
    font-size: 2.8em;
  }

  @media (max-width: 660px) {
    .containerConteudo {
      width: 22em;
    }

    .textoInterativo {
      padding: 0;
      position: static;
      width: 100%;
      text-align: center;
    }

    .imagemInterativo {
      width: 100%;
    }

    h2 {
      font-size: 1.8em;
    }
  }
</style>