<template>
  <v-app>
    <div class="fundo">
      <v-app-bar scroll-target="#scrolling-techniques-7" height="100" >
        <div class="d-flex align-center">
          <button >
            <v-img
              alt="Hokka News Logo"
              class="shrink mr-2 mt-3 mb-3"
              contain
              src="./assets/logo-hokkaido-fogo.png"
              transition="scale-transition"
              width="80%"
              @click="contentChanger('home')"
            />
          </button>
        </div>

        <v-spacer></v-spacer>

        <v-btn text @click="contentChanger('day')">
          <span>Programação</span>
        </v-btn>
        <v-btn text @click="contentChanger('video')">
          <span>Canção</span>
        </v-btn>
        <v-btn text @click="contentChanger('instagram')">
          <span>Notícias</span>
        </v-btn>
        <v-btn text @click="contentChanger('inscricao')">
          <span>Inscrição</span>
        </v-btn>
      </v-app-bar>
      <div class="main">
        <v-content v-if="content === 'home'">
          <Home />
        </v-content>
        <v-content v-else-if="content === 'day'">
          <Day />
        </v-content>
        <v-content v-else-if="content === 'video'">
          <Video />
        </v-content>
        <v-content v-else-if="content === 'instagram'">
          <News />
        </v-content>
        <v-content v-else-if="content === 'inscricao'">
          <div class="forms">
            <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSesK9WUPEBNHfM9zmqFIZVIJgrULFG10DcdRnVoCvEe8itSqQ/viewform?embedded=true" width="100%" height="2800" frameborder="0" marginheight="0" marginwidth="0">Carregando…</iframe>
          </div>
        </v-content>
      </div>
      <div class="teste">
        <Footer />
      </div>
    </div>
  </v-app>
</template>

<script>
import Home from "./components/Home.vue";
import Footer from "./components/Footer.vue";
import Day from "./components/Daily.vue";
import Video from "./components/Video.vue";
import News from "./components/News.vue";



export default {
  name: "App",

  components: {
    Home,
    Footer,
    Day,
    Video,
    News,
  },
  methods: {
    contentChanger: function(content){
      this.content = content
    }
  },
  data: () => ({
    content: 'home',
    drawer: false,
  })
};
</script>

<style scoped>
  .forms{
    background: #dedede;
    width:60%;
    margin:15px auto;
    padding: 15px 0;
    border-radius:5px;
  }
  .forms{
    overflow:hidden;
    padding-bottom:120%;
    position:relative;
    height:0;
  }
  .forms iframe{
    left:0;
    top:0;
    height:100%;
    width:100%;
    position:absolute;
  }
  .fundo{
    background: #0d193c;
  }
  button{
    outline:none
  }
</style>