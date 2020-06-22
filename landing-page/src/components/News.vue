<template>
    <v-content>
        <div class="news">
            <instagram-embed :url="'https://www.instagram.com/p/Bs_yHwHBjKo/'" :max-width="1200"/>
        </div>
    </v-content>
</template>

<script>
import InstagramEmbed from 'vue-instagram-embed';

export default {
    name: 'News',
    components: {
        InstagramEmbed
    },
    data: () => ({
        teste: 'oi'
    }),

}
</script>

<style scoped>
    .news{
        width:80%;
        margin: 50px auto;
        background: #dedede;
    }
div {
    background: #0d193c;
}
</style>