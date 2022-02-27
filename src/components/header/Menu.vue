<template>
  <div class="containerMenu">
    
    
    <!-- PERCORRENDO ARRAY DE ITENS PARA MOSTRAR NO MENU -->
    <nav class="menu">
      <div class="itemMenu" :key="{item}" v-for="item in itensMenu">
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
    display: flex;
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

  @media (max-width: 460px) {
    .menu {
      flex-direction: column;
      width: 50%;
    }

    .itemMenu {
      margin-top: 0%;
      width: 30%;
    }
  }
</style>