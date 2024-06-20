<script>
import JumboSection from "./jumbo/JumboSection.vue";
import VideoAndCallToAction from "./VideoAndCallToAction.vue";
import TrainingAndArticles from "./TrainingAndArticles.vue";
import BannerAndSponsors from "./BannerAndSponsors.vue";
import Events from "./Events.vue";
export default {
    components: {
        JumboSection,
        VideoAndCallToAction,
        TrainingAndArticles,
        BannerAndSponsors,
        Events

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
        <Events />
        <BannerAndSponsors />
    </main>
</template>

<style lang="scss" scoped>

</style>