<script>
import JumboSection from "./jumbo/JumboSection.vue";
import AppCiro from "./AppCiro.vue";
import TrainingAndArticles from "./TrainingAndArticles.vue";
import BannerAndSponsors from "./BannerAndSponsors.vue";
export default {
    components: {
        JumboSection,
        AppCiro,
        TrainingAndArticles,
        BannerAndSponsors

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
        <BannerAndSponsors />
    </main>
</template>

<style lang="scss" scoped>

</style>