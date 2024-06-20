<script>
import AppAdelmo from "./ade_section/JumboSection.vue";
import AppCiro from "./AppCiro.vue";
import AppLorenz from "./TrainingAndArticles.vue";
import AppLuca from "./BannerAndSponsors.vue";
export default {
    components: {
        AppAdelmo,
        AppCiro,
        AppLorenz,
        AppLuca

    },
    data() {
        return {

        }
    }
}
</script>

<template>
    <main>
        <AppAdelmo />
        <AppCiro />
        <AppLorenz />
        <AppLuca />
    </main>
</template>

<style lang="scss" scoped>

</style>