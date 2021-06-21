<template>
    <header>
        <div class="logo">
            <img src="../assets/img/logo-img-01.png" alt="logo_small">
        </div>
        <div class="nav">
            <div 
            v-for="(option) in options"
            :key="option.id"
            >
                <HeaderMenu 
                    :item="option"
                />  
            </div>
            <div>
                <img src="../assets/svg/svg-1.svg">
            </div>
        </div>
        
            
    </header>
</template>

<script>
import HeaderMenu from "./HeaderMenu.vue"

export default {
    name: "Header",

    components: {
        HeaderMenu
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
    }
  }
}
</script>

<style lang="scss" scoped>
    header {
        display: flex;
        align-items: center;
        padding: 30px;
        max-width: 1235px;
        margin: auto;

        .logo {
            flex-grow: 1;
            
            img {
                height: 30px;
            }
        }

        .nav {
            display: flex;
        }
    }
</style>