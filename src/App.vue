<template>
  <div id="app">
    <Header 
      :elements="options"
    /> 

    <Main />

    <Footer
      :items="medias"
    />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },

  data: function () {
    return {
      options: [
        {
          title: "Home",
          id: 1 
        },
        {
          title: "Pages",
          id: 2
        },
        {
          title: "Portfolio",
          id: 3
        },
        {
          title: "Blog",
          id: 4 
        },
        {
          title: "Shop",
          id: 5 
        },
        {
          title: "Elements",
          id: 6 
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
          bgcolor: "green"
        },
      ]
    }
  }

  
}
</script>

<style lang="scss">
@import "./style/general.scss";

</style>
