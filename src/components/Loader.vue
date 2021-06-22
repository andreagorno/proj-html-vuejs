<template>
    <section>
        <img src="../assets/img/logo-img-01.png" alt="logo">
        <img src="../assets/img/ajax-loader.gif" alt="loader">
    </section>
</template>

<script>
export default {
    name: "Loader"
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-color: $bgMainColor1;
        background-image: url("../assets/img/h2-background-img-02.png");
        background-size: contain;
        background-repeat: no-repeat;
        background-position-y: 150px;
    }
</style>