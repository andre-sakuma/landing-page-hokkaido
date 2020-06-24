<template>
  <v-app>
    <v-app-bar app scroll-target="#scrolling-techniques-7" height="100" >
      <div class="d-flex align-center">
        <button >
          <v-img
            alt="Hokka News Logo"
            class="shrink mr-2 mt-3 mb-3"
            contain
            src="./assets/logo-hokkaido-fogo.png"
            transition="scale-transition"
            max-width="250px"
            @click="contentChanger('home')"
          />
        </button>
      </div>

      <v-spacer></v-spacer>

      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            color="primary"
            dark
            text
            v-bind="attrs"
            v-on="on"
          >
            <img src="./assets/menu.svg"/>
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
          >
            <v-list-item-title>
              <v-btn text @click="contentChanger(item.content)">
                {{ item.title }}
              </v-btn>
            </v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <div class="content">
      <v-content v-if="content === 'home'">
        <Home />
        <div class="btnHolder">
          <div class="formButton">
            <v-btn block x-large color="#ff5757"  @click="contentChanger('inscricao')"><p>Faça a sua inscrição!</p></v-btn>
          </div>
        </div>
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
    <Footer />
  </v-app>
</template>


<script>
import Home from "./components/Home.vue";
import Footer from "./components/Footer.vue";
import Video from "./components/Video.vue";
import News from "./components/News.vue";

export default {
  name: "App",
  components: {
    Home,
    Footer,
    Video,
    News,
  },
  methods: {
    contentChanger: function(content){
      this.content = content
    }
  },
  events: {
    'child-msg': function(msg){
      console.log(msg)
      this.contentChanger(msg);
    }
  },
  data: () => ({
    content: 'home',
    drawer: null,
    items: [
      { title: 'Home', content: 'home' },
      { title: 'Canção', content: 'video' },
      { title: 'Notícias', content: 'instagram' },
      { title: 'Inscrição', content: 'inscricao' },
    ],
  }),
  props: {
    source: String
  }
};
</script>

<style scoped>
  span{
    color: #ff5757;
  }
  .forms{
    background: #dedede;
    width:60%;
    margin:50px auto;
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
  .content{
    background: rgb(59, 75, 121)
  }
  .v-main{
    padding:0;
  }
  button{
    outline:none
  }
  .formButton{
    width: 60%;
    margin: 0 auto;    
  }
  .formButton p{
    margin: auto 0;
    color: #dedede;
    font-size: 1.5vw;
  }
  .btnHolder{
    width:100%;
  }
</style>