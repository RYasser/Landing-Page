<template>
  <div class="criacoes">

    <div class="containerCriacoes">

      <!-- CABEÇALHO DOS CARDS, ONDE CONTÉM O TÍTULO DA SEÇÃO E O BOTÃO SEE ALL -->
      <section class="cabecalhoCriacoes">
        <h2 class="tituloSecao">OUR CREATIONS</h2>
        <button class="botaoVerTudo botaoDesktop">SEE ALL</button>
      </section>

      <!-- PERCORRE O ARRAY DE OBJETOS QUE CONTÉM TITULO E IMAGEM REFERENTE AO CARD -->
      <div class="containerCards">
        <Card :urlImagem="card.imagem" v-for="(card, key) in cards" :key="key">
          <h3 class="tituloCard">{{ card.titulo }}</h3>
        </Card>
      </div>

      <!-- BOTÃO COM A CLASSE ESPECÍFICA PARA O DISPLAY MOBILE -->
      <button class="botaoVerTudo botaoMobile">SEE ALL</button>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue"
import { cards } from "../../cards.js"

export default {
  components: {
    Card
  },
  data: function() {
    return {
      // ARRAY DE OBJETOS COM NOME DA IMAGEM QUE ESTÁ NO DIRETÓRIO E O TÍTULO
      cards
    }
  }
}
</script>

<style scoped>
  .criacoes {
    height: auto;
    margin-bottom: 8em;
  }

  .containerCriacoes {
    position: relative;
    left: 6.5em;
    width: 72em;
    height: auto;
    color: hsl(0, 0%, 20%);
  }

  .cabecalhoCriacoes {
    display: flex;
    justify-content: space-between;
  }

  .tituloSecao {
    font-family: Josefin Sans;
    font-size: 2.8em;
  }

  .botaoVerTudo {
    position: relative;
    top: 1.9em;
    border: solid 1px hsl(0, 0%, 10%);
    background-color: white;
    color: hsl(0, 0%, 3%);
    border-radius: 2px;
    font-family: Josefin Sans;
    font-size: 1.2em;
    letter-spacing: 3px;
    height: 2.2em;
    width: 8em;
    font-weight: bold;
  }

  .botaoDesktop {
    display: block;
  }

  .botaoMobile {
    display: none;
  }

  .botaoVerTudo:hover {
    background-color: hsl(0, 0%, 95%);
    cursor: pointer;
  }

  .containerCards {
    display: flex;
    flex-wrap: wrap;
    height: auto;
    justify-content: space-between;
  }

  @media (max-width: 660px) {
    .botaoMobile {
      display: block;
      left: 3.5rem;
    }

    .botaoDesktop {
      display: none;
    }

    .cabecalhoCriacoes {
      position: static;
    }

    .containerCards {
      flex-direction: column;
      overflow: hidden;
      width: 19rem;
    }

    .containerCriacoes {
      position: static;
      width: 18em;
      padding: 0em 0em 0em 5em;
    }

    .tituloSecao {
      font-size: 2.2em;
    }
  }
</style>