<template>
  <div class="containerMenu">
    
    
    <!-- PERCORRENDO ARRAY DE ITENS PARA MOSTRAR NO MENU -->
    <nav class="menu">
      <div class="itemMenu" v-for="item in itensMenu">
        {{ item }}
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      // ITENS DO MENU
      itensMenu: [
      'About',
      'Careers',
      'Events',
      'Products',
      'Support'
    ]
    }
  }
}
</script>

<style scoped>
  .logo {
    float: left;
  }

  .menu {
    float: right;
    margin-right: 75px;
    display: flex;
    font-size: 15px;
  }

  .itemMenu {
    color: white;
    margin: 15px;
    height: 30px;
    width: 100%;
  }

  .itemMenu:hover {
    cursor: pointer;
  }

  @media (max-width: 375px) {
    .containerMenu {
      position: relative;
      left: 40%;
    }

    .menu {
      flex-direction: column;
      margin: 1.5rem 0rem 1.5rem 0rem;
    }

    .itemMenu {
      margin-top: 0%;
    }
  }
</style>