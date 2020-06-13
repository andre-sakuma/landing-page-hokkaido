<template>
  <v-content>
    <div class="base">
      <div class="teste">
        <p>oi</p>
      </div>
    </div>
  </v-content>
</template>

<script>
  export default {
    name: 'Home',

    data: () => ({
      teste: 'oi'
    }),
  }
</script>

<style scoped>
  .base{
    background: red;
  }
  .teste{
    margin: 0 auto;
    background: gray;
  }
  p{
    margin: auto;
  }
</style>