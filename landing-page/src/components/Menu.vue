<template>
  <div class="text-center">
    <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          text
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>
            mdi-home
          </v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>
<script>
  export default {
    data: () => ({
      items: [
        { title: 'Home' },
        { title: 'Cancao' },
        { title: 'Noticias' },
        { title: 'Inscricao' },
      ],
    }),
  }
</script>