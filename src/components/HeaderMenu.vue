<template>
    <div 
    class="items" 
    :class="{'active' : item.id == activeItem}"
    @click="setActive(item.id)">
        {{ item.title }}
    </div>
</template>

<script>
export default {
    name: "HeaderMenu",

    props: [ "item" ],

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
    .items {
        margin-right: 30px;
        font-weight: bold;
        color: $mainTextColor1;
        cursor: pointer;
    }

    .active {
        border-bottom: 2px solid #EFCA9E;
    }
</style>