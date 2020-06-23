<template>
  <div>
    <hr class="rounded">
    <div class="base">
      <div class="group">
        <div class="image">
          <img src="../assets/grupo_todo.jpg" />
        </div>
      </div>
      <div class="redes">
        <div class="content">
          <h2>Contato</h2>
          <v-btn class="contactBtn" text href="https://www.facebook.com/HokkaNews">
            <img class="icon" src="../assets/face-logo.png">
            <span>Facebook</span>
          </v-btn>
          <v-btn class="contactBtn" text href="http://www.instagram.com/hokka_news">
            <img class="icon" src="../assets/insta-logo.png">
            <span>Instagram</span>
          </v-btn>
          <v-btn class="contactBtn" text href="mailto: gehokkaido80@gmail.com">
            <span>Email: Grupo</span>
          </v-btn>
          <v-btn class="contactBtn" text href="mailto: hokklan.hokkaido@gmail.com">
            <span>Email: Clã</span>
          </v-btn>
        </div>
      </div>
    </div>
  </div>
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
  span{
    font-size: 2vw
  }
  h2{
    font-size: 3vw;
    text-align: center;
    margin-bottom: 10px;
    color:#ff5757;
  }
  .icon{
    height:35px;
    width:35px;
    margin-right:15px
  }
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
  .content{
    background:#dedede;
    width:70%;
    padding: 5px;
    margin: 15px auto;
    border-radius: 5px;
  }
  .contactBtn{
    width:100%;
    height: 10%;
    margin-top: 15px ;
  }
  img{
    color: #ff5757;
    width:100%;
    border-radius: 5px;
  }
  div{
    background:rgb(59, 75, 121);
  }
  hr.rounded {
  border-top: 0.5px solid #dedede;
  border-radius: 5px;
  width:90%;
  margin: 100px auto 15px auto;
}
</style>