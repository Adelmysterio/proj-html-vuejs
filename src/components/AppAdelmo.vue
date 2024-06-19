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
                <h1>Take Control of your health</h1>
                <i class="fa-solid fa-stairs fa-rotate-by yellow" style="--fa-rotate-angle: 45deg;"></i>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
                <button><i class="fa-brands fa-youtube"></i> Visit my YouTube channel</button>
                <button>Buy Avada today <i class="fa-solid fa-arrow-right"></i></button>
            </section>
            <button>
                <i class="fa-solid fa-play"></i>
            </button>
        </div>
    </div>
</template>

<style lang=scss scoped>
.bg-img {
    background: linear-gradient(to right, black, black ,black, transparent, transparent), 
                url(https://avada.website/fitness/wp-content/uploads/sites/130/2020/02/slider82x-scaled.jpg);
    background-size: cover;
    height: 700px;
}
section {
    color: white;
    h1 {
        font-size: 4rem;
    }
}
button {
    margin-right: 1rem;
}
</style>