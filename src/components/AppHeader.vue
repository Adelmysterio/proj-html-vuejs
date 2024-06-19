<script>
export default {
    data() {
        return {
            headerLink: [
            {   id: 1,
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
                title: "Store new",
                active: false,
                url: '#'
            }]
        }
    }
}
</script>

<template>
    <header>
        <nav class="d-flex p-5 my-bg-color">
            
            <ul>
                <!--LOGO IMG-->
                <li>
                    <img src="../images/logo-200x34.png" alt="Avada Fitness logo">
                </li>
            </ul>
            
            <ul class="d-flex my-color-li">
                <!--Header link gestiti dinamicamente-->
                <li class="me-4" v-for="headerLink in headerLink" :key="headerLink.id">
                    <a href="">{{ headerLink.title }}</a>
                </li>
                <!--Button-->
                <li>
                    <button>Schedule a workout</button>
                </li>
                <!--Lente font awesome-->
                <li>
                    <i class="fa-solid fa-magnifying-glass"></i>
                </li>
                <!--Carrello font awesome-->
                <li>
                    <i class="fa-solid fa-cart-shopping"></i>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang=scss scoped>
    nav.my-bg-color{
        background-color: #060607;
    }

    ul.my-color-li{
        li{
            color: #757f8a;
        }

        a{
            color: #757f8a;
        }
        

        &:hover{
            color: white;
        }
    }
</style>