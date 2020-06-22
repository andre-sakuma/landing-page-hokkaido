<template>
  <div>
    <div class="fundo">
      <img src="../assets/WIP-logo.png" />
    </div>
  </div>
</template>

<script>
  export default {
    name: 'day',

    data: () => ({
      teste: 'oi',
    }),
  }
</script>

<style scoped>
  .fundo{
    width: 85%;
    margin:0 auto;
    background: #dedede;
  }
  img{
    width:50%;
    margin: 0 auto;
  }
</style>