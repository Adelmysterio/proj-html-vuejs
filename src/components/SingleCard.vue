<script>
export default {
    props: {
        img: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        }
    }
}
</script>

<template>
    <article class="single-card" :style="{ backgroundImage: 'url(' + img + ')' }">
        <section class="content-overlay">
            <i class="fa-solid fa-stairs fa-rotate-by" style="--fa-rotate-angle: 45deg;"></i>
            <h2>{{ title }}</h2>
            <p>{{ description }}</p>
        </section>
    </article>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;

</style>