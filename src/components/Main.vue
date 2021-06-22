<template>
    <main>
        <PageIntro />

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
}
</script>

<style lang="scss" scoped>

</style>