<script>
import JumboSection from "./jumbo/JumboSection.vue";
import VideoAndCallToAction from "./VideoAndCallToAction.vue";
import TrainingAndArticles from "./TrainingAndArticles.vue";
import BannerAndSponsors from "./BannerAndSponsors.vue";
import Events from "./Events.vue";
import FloatingButtons from "./FloatingButtons.vue";
export default {
    components: {
        JumboSection,
        VideoAndCallToAction,
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
        <VideoAndCallToAction />
        <TrainingAndArticles />
        <FloatingButtons />
        <Events />
        <BannerAndSponsors />
    </main>
</template>

<style lang="scss" scoped>


</style>