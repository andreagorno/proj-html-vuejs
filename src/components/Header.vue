<template>
    <header>
        <div class="logo">
            <img src="../assets/img/logo-img-01.png" alt="logo_small">
        </div>
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
            <div>
                <img src="../assets/svg/svg-1.svg">
            </div>
        </div>
        
            
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

          .items {
            margin-right: 30px;
            font-weight: bold;
            color: $mainTextColor1;
            cursor: pointer;
          }
        }
        .active {
        border-bottom: 2px solid #EFCA9E;
    }
    }
</style>