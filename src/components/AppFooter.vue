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
        <nav class="d-flex">
            <!--AVADA FITNESS SOCIAL-->
            <ul>
                <li>
                    <img src="../images/logo-200x34.png" alt="Avada Fitness logo">
                </li>
                <li>
                    <p>
                        Ac aliquam neque sagittis diam faubicus vitae purus turpis phasellus. Pellentesque consectetur amet purus ultrices mauris.
                    </p>
                </li>
                <li>
                    social
                </li>
            </ul>

            <!--AVADA FITNESS LINK DINAMICI-->
            <ul >
                <li>
                    <h6>
                        Recent posts
                    </h6>
                </li>
                <li v-for="footerLink in footerLink" :key="footerLink.id">
                    {{ footerLink.textTitle }}
                </li>
            </ul>

            <!--INFORMATIONS-->
            <ul>
                <li>
                    <h6>
                        Contact informations
                    </h6>
                </li>
                <!--indirizzo-->
                <li>
                    476 Tipple Road Michigan 48449
                </li>
                <!--contacts-->
                <li>
                    <strong>Mobile: 1.800.000.0000</strong>
                </li>
                <li>
                    <strong>Email: info@your-company.com</strong>
                </li>
            </ul>
        </nav>
    </footer>
</template>

<style lang="scss" scoped>
nav{
    background-color: #060607;
}

h6{
    text-transform: uppercase;
}
</style>