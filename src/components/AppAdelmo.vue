<script>
import PlayButton from "./PlayButton.vue";
import JumboContent from "./ade_section/JumboContent.vue";
export default {
    components: {
        PlayButton,
        JumboContent
    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="bg-img d-flex">
        <div class="container-huge d-flex align-items-center justify-content-between w-100">
            <JumboContent />
            <PlayButton />
        </div>
    </div>
    <div>
        <div class="container-huge d-flex align-items-center justify-content-between w-100">

        </div>
    </div>
</template>

<style lang=scss scoped>
.bg-img {
    background: linear-gradient(to right, black, black, black, transparent, transparent),
        url(https://avada.website/fitness/wp-content/uploads/sites/130/2020/02/slider82x-scaled.jpg);
    background-size: cover;
}



</style>