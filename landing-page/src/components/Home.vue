<template>
  <div class="fundo">
    <div class="base">
      <div class="teste">
        <video autoplay muted loop id="myVideo">
          <source src="../assets/terra_em_fogo.mp4" type="video/mp4">
        </video>
      </div>
      <div class="timer">
        <Timer 
         endtime="Jul 11, 2020 20:00:00" 
         trans='{  
         "day":"Day",
         "hours":"Hours",
         "minutes":"Minuts",
         "seconds":"Seconds",
         "expired":"Event has been expired.",
         "running":"Till the end of event.",
         "upcoming":"Till start of event.",
         "status": {
            "expired":"Expired",
            "running":"Running",
            "upcoming":"Future"
           }}'
         ></Timer>
      </div>
    </div>
  </div>
</template>

<script>
  import Timer from "./Timer.vue"
  export default {
    name: 'Home',
    data: () => ({
      teste: 'oi'
    }),
    components:{
      Timer,
    }
  }
</script>

<style scoped>
  .fundo{
    background:rgb(59, 75, 121);
    padding-bottom: 150px;
  }
  video{
    width:100%
  }
  .timer{
    margin: 0 auto;
  }
</style>