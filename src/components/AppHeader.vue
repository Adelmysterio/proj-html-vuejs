<script>
export default {
    data() {
        return {
            activeLens: false,
            headerLink: [
                {
                    id: 1,
                    title: "Home",
                    active: false,
                    url: '#'
                },
                {
                    id: 2,
                    title: "Services",
                    active: false,
                    url: '#'
                },
                {
                    id: 3,
                    title: "About",
                    active: false,
                    url: '#'
                },
                {
                    id: 4,
                    title: "Blog",
                    active: false,
                    url: '#'
                },
                {
                    id: 5,
                    title: "Store",
                    active: false,
                    url: '#'
                }
            ],
        }
    },
    methods: {
        invertInput() {
            console.log(this.activeLens)
            if (this.activeLens === false) {
                this.activeLens = true
            } else {
                this.activeLens = false
            }
        }
    }
}
</script>


//PROVA


<template>
    <header class="my-bg-color">
        <nav class="d-flex justify-content-between container-huge align-items-center">

            <!--LOGO IMG-->

            <img src="../images/logo-200x34.png" alt="Avada Fitness logo">
            
            <ul class="d-flex align-items-center my-color-li">

                <!--Header link gestiti dinamicamente-->
                <li class="me-4" v-for="headerLink in headerLink" :key="headerLink.id">
                    <a href="">{{ headerLink.title }}</a>
                </li>

                <li>

                </li>

                <!--Button search-->
                <li class="me-4">
                    <button>Schedule a workout</button>
                </li>

                <!--Button lens-->
                <li class="me-4">
                    <button @click="invertInput()" class="my-lens my-display"><i
                            class="fa-solid fa-magnifying-glass"></i></button>
                    <input :class="activeLens === false ? 'my-hidden' : 'my-visible'" type="text">
                </li>

                <!--Carrello font awesome-->
                <li>
                    <a href=""><i class="fa-solid fa-cart-shopping"></i></a>
                </li>
            </ul>

        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

nav {
    padding: 1rem 0;
}

a {
    text-decoration: none;
}

.my-bg-color {
    background-color: $bg-black;
}

ul.my-color-li {
    li {
        color: $color-grey;
    }

    a {
        color: $color-grey;

        &:hover {
            color: white;
        }
    }
}

// Classi per funzionamento dell'input comparsa e scomparsa. NON inserire nello style generale scss
button.my-lens {
    border: none;
    background-color: $bg-black;
    color: $color-grey;

    &:hover {
        color: white;
    }
}

input.my-hidden {
    display: none;
}

input.my-visible {
    display: inline-block;
}
</style>