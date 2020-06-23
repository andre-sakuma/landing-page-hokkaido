<template>
  <div class="fundo">
    <div class="base">
      <div class="video">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/qhiDyybGjWk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <h1>INTRODUCAO</h1>
      <p>Olá, gostaria de cantar a canção da despedida do fogo de conselho com a gente? Apesar da pandemia ainda estar acontecendo, mesmo estando em sua casa, isso ainda é possível!
        Neste 38º fogo de conselho, você não estará sozinho!
      </p>
      <p>A seguir, estão as etapas para que você consiga cantar junto a todos nós:</p>
      <h2>1ª Etapa</h2>
      <p>Use esta a música de acompanhamento abaixo para cantar com a gente:</p>
      <div class="videoresize">
        <div class="video2">
          <iframe width="560" height="315" src="https://www.youtube.com/embed/qhiDyybGjWk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
      </div>
      <h2>2ª Etapa</h2>
      <p>Faça um vídeo dentro de sua casa. Ao ligar a câmera:</p>
      <ul>
        <li>Diga seu nome para a câmera.</li>
        <li>Dê seus cumprimentos, acene etc. para a câmera por 5 segundos. </li>
        <li>Dê um play na música de acompanhamento.</li>
        <li>O vídeo deve ser gravado em modo retrato.</li>
      </ul>
      <h2>3ª Etapa</h2>
      <p>Mande-nos o vídeo pelo WeTransfer.
      <br>Como fazer isso? Simples.
      </p>
      <ul>
        <li>Primeiro, acesse o link <a href="https://www.wetransfer.com">https://www.wetransfer.com</a></li>
        <li>Clique em adicionar ficheiros. </li>
        <li>Selecione o arquivo do vídeo gravado.</li>
        <li>Clique no círculo com reticências e selecione para obter link.</li>
        <li>Clique em obter link.</li>
        <li>Copie o link obtido e mande-nos por Whatsapp ou email.</li>
      </ul>

    </div>
  </div>
</template>

<script>
  export default {
    name: 'Video',

    data: () => ({
      teste: 'oi'
    }),
  }
</script>

<style scoped>
  ul{
    color:#ff5757;
  }
  a{
    color:#ff5757;
  }
  h1{
    margin-top: 50px;
    color: #ff5757;
  }
  h2{
    color: #ff5757;
    margin-top: 50px;
  }
  p{
    font-size:large;
    color: #ff5757;
  }
  .fundo{
    background:rgb(59, 75, 121);
    padding:50px 0
  }
  .base{
    width:80%;
    margin: 0 auto;
    padding: 30px 30px 60px 30px;
    border-radius: 5px;
    background: #dedede;
  }
  .video{
    overflow:hidden;
    padding-bottom:56.25%;
    position:relative;
    height:0;
  }
  .video iframe{
    left:0;
    top:0;
    height:100%;
    width:100%;
    position:absolute;
  }
  .videoresize{
    width:50%
  }
  .video2{
    overflow:hidden;
    padding-bottom:56.25%;
    position:relative;
    height:0;
  }
  .video2 iframe{
    left:0;
    top:0;
    height:100%;
    width:100%;
    position:absolute;
  }
  .teste{
  }
</style>