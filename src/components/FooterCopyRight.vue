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
                Copyright 2012 - 2020|Avada theme by <a class="text-white">ThemeFusion</a>|All rights reserved|Powered by <a class="text-white">WordPress</a>
            </p>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
a{
    text-decoration: none;

    &:hover{
        color: #4154ff!important;
    }
}

section.my-bg-color{
    background-color: #060607;
}

.my-color-grey{
    color: #abaaad;
}

</style>