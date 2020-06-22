<template>
  <v-content>
    <div class="base">
      <div class="video">
        <iframe width="420" height="315" src="https://www.youtube.com/embed/xoI-38QvLSA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>      
      </div>
    </div>
  </v-content>
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
  .base{
    width:80%;
    margin: 50px auto;
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
  .teste{
  }
</style>