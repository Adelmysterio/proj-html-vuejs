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
@use '../../style/partials/variables.scss' as *;

.single-card {
    width: 30%;
    background-size: cover;
    background-repeat: no-repeat;
    border-radius: 5px 5px 40px 5px;
    overflow: hidden;
    position: relative;
    top: -100px;
}

.content-overlay {
    color: white;
    padding: 90% 10% 5%;
    background-image: linear-gradient(to top, rgba(0, 0, 0, 0.897), transparent);

    i {
        font-size: 1.5rem;
    }

    h2 {
        font-weight: bold;
    }

    p {
        color: $yellow;
        font-size: 1.7rem;
    }
}
</style>