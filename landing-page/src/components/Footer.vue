<template>
  <v-content>
    <div class="base">
      <div class="group">
        <div class="image">
          <img src="../assets/grupo_todo.jpg" />
        </div>
      </div>
      <div class="redes">
        <v-btn text href="https://www.facebook.com/HokkaNews">
          <span>Facebook</span>
        </v-btn>
        <v-btn text href="http://www.instagram.com/hokka_news">
          <span>Instagram</span>
          <v-icon>

          </v-icon>
        </v-btn>
      </div>
    </div>
  </v-content>
</template>

<script>
  export default {
    name: 'Footer',

    data: () => ({
      teste: 'oi'
    }),
    
  }
</script>

<style scoped>
  .base{
    display:flex;
  }
  .group{
    width:50%;
  }
  .redes{
    width:50%;
  }
  .image{
    width:70%;
    margin: 15px auto;
  }
  img{
    width:100%;

  }
  div{
    background:#0d193c;
  }
</style>