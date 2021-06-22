<template>
    <main>
        <PageIntro 
        :items="infos"
        />

        <WhatWeDo />

        <LearnMore />
    </main>
</template>

<script>
import PageIntro from "./PageIntro.vue";
import WhatWeDo from "./WhatWeDo.vue";
import LearnMore from "./LearnMore.vue";

export default {
    name: "Main",

    components: {
        PageIntro,
        WhatWeDo,
        LearnMore
    },

    data: function () {
        return {
            infos: [
                {
                    poster: "port-img-07.jpg",
                    h4: "City Paysage",
                    h5: "Book illustrations"
                },
                {
                    poster: "port-img-08.jpg",
                    h4: "Free design",
                    h5: "Book illustrations"
                },
                {
                    poster: "port-img-09.jpg",
                    h4: "Green cards",
                    h5: "Book illustrations"
                },
                {
                    poster: "port-img-10.jpg",
                    h4: "Rainy day",
                    h5: "Book illustrations"
                },
                {
                    poster: "port-img-11.jpg",
                    h4: "John & Martha",
                    h5: "Book illustrations"
                },
                {
                    poster: "port-img-12.jpg",
                    h4: "Millions of cats",
                    h5: "Book illustrations"
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>