<template>
  <header id="top">
    <!-- logo start -->
    <div class="logo">
        <img src="../assets/img/logo-img-01.png" alt="logo_small">
    </div>
    <!-- /logo start -->

    <!-- nav-bar start -->
    <div class="nav">
      <div 
        v-for="element in elements"
        :key="element.id"
        class="items"
        :class="{'active' : element.id == activeItem}"
        @click="setActive(element.id)"
      >
      {{ element.title }}     
      </div>
      <div class="dotmenu">
        <i 
        :class="`fas fa-circle ${element.color}`"
        v-for="element in elements"
        :key="element.id"
        ></i> 
      </div>
    </div>
    <!-- /nav-bar start -->

    <!-- triangle toTheTop start -->
    <a href="#top" id="toTop">
      <span class="triangle">
        <i class="fas fa-chevron-up"></i>
      </span>
    </a>
    <!-- /triangle toTheTop start -->   
            
  </header>
</template>

<script>


export default {
    name: "Header",

    props: {
      elements: [ Array ],
    },

    data: function () {
      return {
        activeItem: 1,
      }
    },

    methods: {
      setActive: function (newActive) {
        console.log(newActive);
        this.activeItem = newActive;
      }
    }
}
  
</script>

<style lang="scss" scoped>
  
  @import "../style/variables.scss";
  #toTop {
    position: fixed;
    top: 90vh;
    right: 20px;
    z-index: 10;

    .triangle {
      border-style: solid;
      border-width: 0 40px 40px;
      border-color: transparent transparent #f6c0ab;

      i {
        position: absolute;
        top: 42px;
        right: 34px;
        color: white;
        font-size: 10px;
        transition: all 1s;
      }
    }
    .triangle:hover i {
      transform: rotate(360deg);
    }
  }
  header {
        display: flex;
        align-items: center;
        padding: 30px;
        max-width: 1600px;
        margin: auto;

        .logo {
            flex-grow: 1;
            
            img {
                height: 30px;
            }
        }

        .nav {
          display: flex;
          align-items: center;

          .items {
            margin-right: 30px;
            font-weight: bold;
            color: $mainTextColor1;
            cursor: pointer;
            transition: all 0.5s;
          }
          .items:hover {
            transform: scale(1.2);
          }
        }
        .active {
        border-bottom: 2px solid #EFCA9E;
        transform: scale(1.2);
        }

        .dotmenu {
          display: flex;
          flex-wrap: wrap;
          width: 50px;
          cursor: pointer;

          i {
            font-size: 6px;
            margin: 4px;
          }
          
        }
    }
</style>

          
