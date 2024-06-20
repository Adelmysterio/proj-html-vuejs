<script>
import FooterCopyRight from './FooterCopyRight.vue';

export default {
    components:{
        FooterCopyRight,
    },
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
        <nav class="d-flex justify-content-between text-center">
            <!--AVADA FITNESS SOCIAL-->
            <ul>

                <!--logo img-->
                <li>
                    <img src="../images/logo-200x34.png" alt="Avada Fitness logo">
                </li>
                <li>
                    <p class="my-color-grey mb-5">
                        Ac aliquam neque sagittis diam faubicus vitae<br> purus turpis phasellus. Pellentesque consectetur<br> amet purus ultrices mauris.
                    </p>
                </li>
                <!--link social-->
                <li>
                    <a href="https://www.facebook.com/?locale=it_IT"><i class="fa-brands fa-facebook-f me-3 my-color-red"></i></a>
                    <a href="https://x.com/?lang=it"><i class="fa-brands fa-x-twitter me-3 my-color-red"></i></a>
                    <a href="https://www.youtube.com/?app=desktop&hl=it"><i class="fa-brands fa-youtube me-3 my-color-red"></i></a>
                    <a href="https://www.instagram.com/"><i class="fa-brands fa-instagram me-3 my-color-red"></i></a>
                    <a href="https://it.linkedin.com/?src=go-pa&trk=sem-ga_campid.20677489327_asid.153452322614_crid.677545198980_kw.linkedin_d.c_tid.kwd-148086543_n.g_mt.e_geo.1008559&mcid=7120409760495009793&cid=&gad_source=1&gclid=CjwKCAjwg8qzBhAoEiwAWagLrDcs3ERJorzxY4XcC9FDk_n8PHbngaGEJo4fdDM_PQxrNRUllbhiaxoCqM0QAvD_BwE&gclsrc=aw.ds"><i class="fa-brands fa-linkedin-in my-color-red"></i></a>
                </li>
            </ul>

            <!--AVADA FITNESS LINK DINAMICI-->
            <ul >
                <li>
                    <h6 class="mb-3">
                        Recent posts
                    </h6>
                </li>
                <li class="mb-4 my-li-a-color-hover" v-for="footerLink in footerLink" :key="footerLink.id">
                    <i class="fa-solid fa-chevron-right me-1"></i>
                    <a class="my-li-a-color-hover" href="">{{ footerLink.textTitle }}</a>
                </li>
            </ul>

            <!--INFORMATIONS-->
            <ul>
                <li>
                    <h6 class="mb-4">
                        Contact informations
                    </h6>
                </li>
                <!--indirizzo-->
                <li class="mb-3 my-color-grey">
                    476 Tipple Road Michigan 48449
                </li>
                <!--contacts-->
                <li>
                    <strong>Mobile: 1.800.000.0000</strong>
                </li>
                <li>
                    <strong>
                        <a href="https://www.microsoft.com/it-it/microsoft-365/outlook/email-and-calendar-software-microsoft-outlook?market=it">
                            Email: info@your-company.com
                        </a>
                    </strong>
                </li>
            </ul>
        </nav>

        <FooterCopyRight/>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/partials/mixins' as*;
@use '../style/partials/variables' as*;

footer{
    font-size: 1.1rem;
}

.my-li-a-color-hover{
    &:hover{
        color: $color-blue;
    }
}

a{
    text-decoration: none;
}

footer{
    width: 100vw;
}

nav{
    padding: 10rem;
    background-color: $bg-black;

    li{
        color: white;
    }

    a{
        color: white;
    }
}

.my-color-grey{
    color: $color-grey;
}

.my-color-red{
    color: #ce353d;
}

h6{
    text-transform: uppercase;
}
</style>