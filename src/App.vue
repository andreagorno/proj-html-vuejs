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
          color: "blue", 
          listOne: false,
          subMenu1: "Main home",
          subMenu2: "Portfolio pinterest",
          subMenu3: "Agency home",
          subMenu4: "Design studio",
          subMenu5: "Illustrator portfolio",
        },
        {
          title: "Pages",
          id: 2,
          color: "lightgreen",
          listOne: false,
          subMenu1: "About us",
          subMenu2: "About me",
          subMenu3: "Our services",
          subMenu4: "Our team",
          subMenu5: "Get in touch",
        },
        {
          title: "Portfolio",
          id: 3,
          color: "orange",
          listOne: false,
          subMenu1: "Standard",
          subMenu2: "Gallery",
          subMenu3: "Gallery joined",
          subMenu4: "Pinterest",
          subMenu5: "Masonry",
        },
        {
          title: "Blog",
          id: 4,
          color: "pink", 
          listOne: false,
          subMenu1: "Mansory list",
          subMenu2: "Right sidebar",
          subMenu3: "Left sidebar",
          subMenu4: "No sidebar",
          subMenu5: "Post types",
        },
        {
          title: "Shop",
          id: 5,
          color: "yellow",
          listOne: false,
          subMenu1: "Product list",
          subMenu2: "Product single",
          subMenu3: "Layouts",
          subMenu4: "Pages",
          subMenu5: "Items", 
        },
        {
          title: "Elements",
          id: 6,
          color: "green",
          listOne: false,
          subMenu1: "Accordions",
          subMenu2: "Tabs",
          subMenu3: "Buttons",
          subMenu4: "Call to action",
          subMenu5: "Clients", 
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
