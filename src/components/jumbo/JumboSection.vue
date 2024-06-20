<script>
import PlayButton from "../PlayButton.vue";
import JumboContent from "./JumboContent.vue";
import SingleCard from "./SingleCard.vue";
import QuoteElement from "./QuoteElement.vue";
export default {
    components: {
        PlayButton,
        JumboContent,
        SingleCard,
        QuoteElement
    },
    data() {
        return {
            articles: [
                {
                    img: 'https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/service6@2x.jpg',
                    title: 'Crossfit workout',
                    description: 'Push your limit',
                },
                {
                    img: 'https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/box1@2x.jpg',
                    title: 'New gym apparel',
                    description: 'Look good, feel good',
                },
                {
                    img: 'https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/box3@2x.jpg',
                    title: 'Team training',
                    description: 'Find a partner',
                },
            ]
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
    <div class="bg-gradient">
        <div class="container-huge">
            <div class="wrapper">
                <SingleCard v-for="(item, index) in articles" :key="index" :img="item.img" :title="item.title"
                    :description="item.description" />
            </div>
            <QuoteElement />
        </div>
    </div>
</template>

<style lang=scss scoped>
@use '../../style/partials/variables.scss' as *;

.bg-img {
    background: linear-gradient(to right, black, black, black, transparent, transparent),
        url(https://avada.website/fitness/wp-content/uploads/sites/130/2020/02/slider82x-scaled.jpg);
    background-size: cover;
}

.bg-gradient {
    background-image: linear-gradient(325deg, red, blue) !important;
    padding-bottom: 15rem;
}

.wrapper {
    display: flex;
    justify-content: space-between;
}
</style>