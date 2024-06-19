<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <section class="fw-bold">
        <p class="red">Certified fitness professional</p>
        <h1>Take control of your health</h1>
        <i class="fa-solid fa-stairs fa-rotate-by yellow" style="--fa-rotate-angle: 45deg;"></i>
        <p class="gray">Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
        <button><i class="fa-brands fa-youtube"></i> Visit my YouTube channel</button>
        <button class="no-bg">Buy Avada today <i class="fa-solid fa-arrow-right"></i></button>
    </section>
</template>

<style lang=scss scoped>
section {
    color: white;
    padding: 6rem 0 15rem 0;

    p.red {
        font-size: 2rem;
    }

    h1 {
        font-size: 4rem;
    }

    
    button {
        margin-right: 1rem;
        margin-top: 2rem;
    }
}

section>i {
    font-size: 4rem;
    margin-bottom: 1rem;
}
</style>