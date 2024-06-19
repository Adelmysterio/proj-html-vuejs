<script>
export default {
    data() {
        return {
            activeLens: false,
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
            }],
        }
    },
    methods:{
        invertInput(){
            console.log(this.activeLens)
            if(this.activeLens === false){
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
        <nav class="d-flex justify-content-evenly p-5 my-bg-color">
            
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
                
                <!--Button search-->
                <li class="me-4">
                    <button>Schedule a workout</button>
                </li>
                
                <!--Button lens-->
                <li class="me-4">
                    <button @click="invertInput()" class="my-lens my-display"><i class="fa-solid fa-magnifying-glass"></i></button>
                    <input :class="activeLens  === false ? 'my-hidden' : 'my-visible'" type="text">
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
    a{
        text-decoration: none;
    }
    
    nav.my-bg-color{
        background-color: #060607;
    }

    ul.my-color-li{
        li{
            color: #757f8a;
        }

        a{
            color: #757f8a;

            &:hover{
                color: white;
            }
        }
    }

    // Classi per funzionamento dell'input comparsa e scomparsa. NON inserire nello style generale scss
    button.my-lens{
        border: none;
        background-color: #060607;
        color: #757f8a;

        &:hover{
            color: white;
        }
    }

    input.my-hidden{
        display: none;
    }

    input.my-visible{
        display: inline-block;
    }
</style>