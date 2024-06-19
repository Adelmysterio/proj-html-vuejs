<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <section class="d-flex flex-column">
        <h2>“How you respond to the challenge in the second half will determine what you become after the game, whether
            you are a winner or a loser.”</h2>
        <i class="fa-solid fa-stairs fa-rotate-by yellow" style="--fa-rotate-angle: 45deg;"></i>
        <div class="d-flex align-items-center">
            <img src="https://avada.website/fitness/wp-content/uploads/sites/130/2020/03/avatar-1@2x.jpg" alt="">
            <p>Brad Johnson</p>
            <span class="gray">Las Vegas</span>
        </div>
    </section>
</template>

<style lang=scss scoped>
@use '../../style/partials/variables.scss' as *;

section {
    width: 80%;
    margin: 0 auto;
    text-align: center;

    h2 {
        font-size: 3.3rem;
        font-weight: bold;
        margin-bottom: 1rem;
    }

    i {
        font-size: 3rem;
        margin-bottom: 1rem;
    }

    img {
        width: 6rem;
        aspect-ratio: 1/1;
        border-radius: 50%;
    }

    div {
        margin: 0 auto;
        font-size: 1.5rem;
        p {
            margin: 0 1rem;
        }
    }
}
</style>