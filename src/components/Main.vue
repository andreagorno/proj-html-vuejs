<template>
    <main>
        <PageIntro />

        <WhatWeDo />
    </main>
</template>

<script>
import PageIntro from "./PageIntro.vue";
import WhatWeDo from "./WhatWeDo.vue";

export default {
    name: "Main",

    components: {
        PageIntro,
        WhatWeDo
    },
}
</script>

<style lang="scss" scoped>

</style>