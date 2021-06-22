<template>
  <div id="app">
    <div v-if="!loader">
      <Header 
      :elements="options"
      /> 

      <Main />

      <Footer
        :items="medias"
      />
    </div>
    
    
    <Loader v-else />
    
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import Loader from "./components/Loader.vue";

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Loader
  },

  data: function () {
    return {
      options: [
        {
          title: "Home",
          id: 1,
          color: "blue" 
        },
        {
          title: "Pages",
          id: 2,
          color: "lightgreen"
        },
        {
          title: "Portfolio",
          id: 3,
          color: "orange"
        },
        {
          title: "Blog",
          id: 4,
          color: "pink" 
        },
        {
          title: "Shop",
          id: 5,
          color: "yellow" 
        },
        {
          title: "Elements",
          id: 6,
          color: "green" 
        }
      ],
      medias: [
        {
          url: "https://www.instagram.com/qodeinteractive/",
          code: "fa-instagram",
          bgcolor: "blue"
        },
        {
          url: "https://www.facebook.com/QodeInteractive/",
          code: "fa-facebook-f",
          bgcolor: "yellow"
        },
        {
          url: "https://twitter.com/QodeInteractive",
          code: "fa-twitter",
          bgcolor: "pink"
        },
        {
          url: "https://www.pinterest.it/qodeinteractive/_created/",
          code: "fa-pinterest-p",
          bgcolor: "lightgreen"
        },
      ],
      loader: true
    }
  },

  created: function () {
    setTimeout( () => {
      this.loader = false;
    },1500)
  }

  
}
</script>

<style lang="scss">
@import "./style/general.scss";

</style>
