<script>
export default {
    data() {
        return {
            footerLink: [
            {
                id: 1,
                textTitle: "The best protein shake",
                active: false,
                url: '#'
            },
            {
                id: 2,
                textTitle: "Ultimate cardio workout",
                active: false,
                url: '#'
            },
            {
                id: 3,
                textTitle: "New juices available now",
                active: false,
                url: '#'
            },
            {
                id: 4,
                textTitle: "Tips to find training partners",
                active: false,
                url: '#'
            },
            {
                id: 5,
                textTitle: "20 best healthy recipes",
                active: false,
                url: '#'
            }],
        }
    }
}
</script>

<template>
    <footer>
        <nav class="d-flex justify-content-evenly text-center">
            <!--AVADA FITNESS SOCIAL-->
            <ul>
                <li>
                    <img src="../images/logo-200x34.png" alt="Avada Fitness logo">
                </li>
                <li>
                    <p class="my-color-grey">
                        Ac aliquam neque sagittis diam faubicus vitae<br> purus turpis phasellus. Pellentesque consectetur<br> amet purus ultrices mauris.
                    </p>
                </li>
                <li>
                    social
                </li>
            </ul>

            <!--AVADA FITNESS LINK DINAMICI-->
            <ul >
                <li>
                    <h6 class="mb-3">
                        Recent posts
                    </h6>
                </li>
                <li class="mb-2" v-for="footerLink in footerLink" :key="footerLink.id">
                    <a href="">{{ footerLink.textTitle }}</a>
                </li>
            </ul>

            <!--INFORMATIONS-->
            <ul>
                <li>
                    <h6 class="mb-3">
                        Contact informations
                    </h6>
                </li>
                <!--indirizzo-->
                <li class="mb-2 my-color-grey">
                    476 Tipple Road Michigan 48449
                </li>
                <!--contacts-->
                <li>
                    <strong>Mobile: 1.800.000.0000</strong>
                </li>
                <li>
                    <strong>
                        <a href="">
                            Email: info@your-company.com
                        </a>
                    </strong>
                </li>
            </ul>
        </nav>
    </footer>
</template>

<style lang="scss" scoped>
a{
    text-decoration: none;
}

footer{
    width: 100vw;
}

nav{
    padding: 10rem;
    background-color: #060607;

    li{
        color: white;
    }

    a{
        color: white;
    }
}

.my-color-grey{
    color: #abaaad;
}

h6{
    text-transform: uppercase;
}
</style>