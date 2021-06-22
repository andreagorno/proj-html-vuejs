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
      ]
    }
  }

  
}
</script>

<style lang="scss">
@import "./style/general.scss";

</style>
