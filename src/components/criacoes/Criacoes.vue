<template>
  <div class="criacoes">

    <div class="containerCriacoes">

      <!-- CABEÇALHO DOS CARDS, ONDE CONTÉM O TÍTULO DA SEÇÃO E O BOTÃO SEE ALL -->
      <section class="cabecalhoCriacoes">
        <h2 class="tituloSecao">OUR CREATIONS</h2>
        <button class="butaoVerTudo">SEE ALL</button>
      </section>

      <!-- PERCORRE O ARRAY DE OBJETOS QUE CONTÉM TITULO E IMAGEM REFERENTE AO CARD -->
      <div class="containerCards">
        <Card :urlImagem="card.imagem" v-for="(card, key) in cards" :key="key">
          <h3 class="tituloCard">{{ card.titulo }}</h3>
        </Card>
      </div>

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
    left: 9em;
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

  .butaoVerTudo {
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

  .butaoVerTudo:hover {
    background-color: hsl(0, 0%, 95%);
    cursor: pointer;
  }

  .containerCards {
    display: flex;
    flex-wrap: wrap;
    height: auto;
    justify-content: space-between;
  }

  @media (max-width: 375px) {
    .butaoVerTudo {
      display: none;
    }

    .cabecalhoCriacoes {
      position: static;
    }

    .containerCards {
      flex-direction: column;
    }

    .containerCriacoes {
      position: static;
      width: 18em;
      padding: 1.5em 4em 1.5em 4em;
    }

    .tituloSecao {
      font-size: 2.2em;
    }
  }
</style>