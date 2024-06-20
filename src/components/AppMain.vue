<script>
import AppAdelmo from "./ade_section/AppAdelmo.vue";
import AppCiro from "./AppCiro.vue";
import AppLorenz from "./AppLorenz.vue";
import AppLuca from "./AppLuca.vue";
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

<style lang=scss scoped></style>