<script>
import JumboSection from "./jumbo/JumboSection.vue";
import AppCiro from "./AppCiro.vue";
import TrainingAndArticles from "./TrainingAndArticles.vue";
import BannerAndSponsors from "./BannerAndSponsors.vue";
import Events from "./Events.vue";
import FloatingButtons from "./FloatingButtons.vue";
export default {
    components: {
        JumboSection,
        AppCiro,
        TrainingAndArticles,
        BannerAndSponsors,
        Events,
        FloatingButtons,

    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <main>
        <JumboSection />
        <AppCiro />
        <TrainingAndArticles />
        <FloatingButtons />
        <Events />
        <BannerAndSponsors />
    </main>
</template>

<style lang="scss" scoped>


</style>