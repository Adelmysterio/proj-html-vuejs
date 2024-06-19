<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="bg-img d-flex">
        <div class="container-huge d-flex align-items-center justify-content-between w-100">
            <section class="fw-bold">
                <p class="red">Certified fitness professional</p>
                <h1>Take control of your health</h1>
                <i class="fa-solid fa-stairs fa-rotate-by yellow" style="--fa-rotate-angle: 45deg;"></i>
                <p class="gray">Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
                <button><i class="fa-brands fa-youtube"></i> Visit my YouTube channel</button>
                <button class="no-bg">Buy Avada today <i class="fa-solid fa-arrow-right"></i></button>
            </section>
            <button class="play">
                <i class="fa-solid fa-play"></i>
            </button>
        </div>
    </div>
</template>

<style lang=scss scoped>
.bg-img {
    background: linear-gradient(to right, black, black, black, transparent, transparent),
        url(https://avada.website/fitness/wp-content/uploads/sites/130/2020/02/slider82x-scaled.jpg);
    background-size: cover;
}

section {
    color: white;
    padding: 6rem 0;

    p.red {
        font-size: 2rem;
    }


    h1 {
        font-size: 4rem;
    }
}

.play {
    font-size: .8rem;
}

section>i {
    font-size: 4rem;
}

button {
    margin-right: 1rem;
}
</style>