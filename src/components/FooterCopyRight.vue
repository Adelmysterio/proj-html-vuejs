<script>

export default {
    data() {
        return {

        }
    },
    props:{
        FooterCopyRight: Object
    }
}
</script>

<template>
    <footer>
        <section class="p-4 text-center border-top my-bg-color">
            <p class="my-color-grey">
                Copyright 2012 - 2020|Avada theme by <spa class="text-white">ThemeFusion</spa>|All rights reserved|Powered by <span class="text-white">WordPress</span>
            </p>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
section.my-bg-color{
    background-color: #060607;
}

.my-color-grey{
    color: #abaaad;
}
</style>