<script>
export default {
    data() {
        return {
            activeLens: false,
            headerLink: [
                {
                    id: 0,
                    title: "Home",
                    active: false,
                    icons: false,
                    url: '#'
                },
                {
                    id: 1,
                    title: "Services",
                    active: true,
                    icons: true,
                    url: '#'
                },
                {
                    id: 2,
                    title: "About",
                    active: true,
                    icons: true,
                    url: '#'
                },
                {
                    id: 3,
                    title: "Videos",
                    active: true,
                    icons: true,
                    url: '#'
                },
                {
                    id: 4,
                    title: "Blog",
                    active: false,
                    icons: false,
                    url: '#'
                },
                {
                    id: 5,
                    title: "Store new",
                    active: true,
                    icons: true,
                    url: '#'
                },
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

<template>
    <header>

        <nav class="navbar navbar-expand-lg bg-body-tertiary my-bg-color p-3 d-flex justify-content-center">
            <img src="../images/logo-200x34.png" alt="Avada Fitness logo">
                <!--Img e botton fluid a scomparsa-->
                <div class="container-fluid">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                
                    <!--Headerlink title-->
                    <div class="collapse navbar-collapse" id="navbarScroll">
                        <ul class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
                            <li class="nav-item dropdown" v-for="headerLink in headerLink" :key="headerLink.id">
                            <a class="nav-link dropdown-toggle text-white" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                {{ headerLink.title }}
                            </a>
                        
                            <!--Dropdown menù-->
                            <ul class="dropdown-menu">
                                <li>
                                    <a class="dropdown-item" href="#">
                                        All Services
                                    </a>
                                </li>
                                <li>
                                    <a class="dropdown-item" href="#">
                                        Simple Product
                                    </a>
                                </li>
                                <li>
                                    <a class="dropdown-item" href="#">
                                        All playlist
                                    </a>
                                </li>
                                <li>
                                    <a class="dropdown-item" href="#">
                                        Dropdown
                                    </a>
                                </li>
                                <li>
                                    <a class="dropdown-item" href="#">
                                        All Playlist
                                    </a>
                                </li>
                            </ul>

                            <!--Chiusura primo ul con li-->
                            </li>
                        </ul>
            
                <!--Form, bottone, input e icons-->
                <form class="d-flex" role="search">
                <li class="me-4">
                    <button>Schedule a workout</button>
                </li>
                <button @click="invertInput()" class="my-lens my-display">
                    <i class="fa-solid fa-magnifying-glass"></i>
                </button>
            </form>
            <input :class="activeLens === false ? 'my-hidden' : 'my-visible'" type="text">
            <span><i class="fa-solid fa-cart-shopping m-3 my-color"></i></span>
        </div>
    </div>
</nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;
@use '../style/general.scss' as*;

.my-bg-color {
    background-color: $bg-black!important;
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

input{
    border-radius: 1rem;
    width: 200px;
}

i.my-color{
    color: white;
}
</style>