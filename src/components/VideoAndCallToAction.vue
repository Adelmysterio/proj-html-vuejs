<script>
import PlayButton from './PlayButton.vue';
export default {
    components: {
        PlayButton
    },
    data() {
        return {
            CardData: [
                { id: 0, title: 'Thighs & glute workout', image: 'https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/video2@2x.jpg', link: 'Increase your mobility' },
                { id: 1, title: 'Lift, firm & perk up', image: 'https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/video7@2x.jpg', link: 'Feel young again' },
                { id: 2, title: 'Slim & trim your waist', image: 'https://avada.website/fitness/wp-content/uploads/sites/130/2019/12/video9@2x.jpg', link: 'Shed those extra pounds' },

            ],
            ArticleData: [
                {
                    id: 0,
                    title: 'The best health & fitness advice online',
                    text: 'Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper mauris, venenatis, leo integer sit pellentesque.',
                    link: 'Tune up your workouts',
                },
            ],
        };
    }
}
document.addEventListener("DOMContentLoaded", function () {
    const scrollElements = document.querySelectorAll('.hidden-scroll');
    const checkVisibility = () => {
        scrollElements.forEach((element) => {
            const rect = element.getBoundingClientRect();
            if (rect.top <= (window.innerHeight || document.documentElement.clientHeight) && rect.bottom >= 0){
                setTimeout(() =>{
                    element.classList.add('visible-scroll');
                }, 400);
                
            }
        });
    };
    window.addEventListener('scroll', checkVisibility);
    
    
    checkVisibility();
});
</script>

<template>

    <div>
        <div class="workouts d-flex w-100">
            <figure class="single-card hidden-scroll">
                <PlayButton class="hidden-scroll"/>
            </figure>
            <section class="caption d-flex flex-column justify-content-center hidden-scroll" v-for="item in ArticleData">
                <p class="link">{{ item.link }}</p>
                <h4 class="title">{{ item.title }}</h4>
                <p class="text gray"> {{ item.text }}</p>
                <button class="bg-red"><i class="fa-brands fa-youtube"></i> Visit my YouTube channel</button>
            </section>
        </div>
        <div class="playlist container-huge d-flex flex-column hidden-scroll">
            <h2 class="mb-5">Feautred playlists</h2>
            <div class="wrapper">
                <article v-for="item in CardData" :key="item.id" class="video-container hidden-scroll">
                    <div class="video single-card mb-5" :style="{ backgroundImage: 'url(' + item.image + ')' }" :key="item.id">
                        <PlayButton />
                    </div>
                    <section class="text-center fw-bold hidden-scroll">
                        <h3>{{ item.title }}</h3>
                        <a :href="item.link">{{ item.link }}</a>
                    </section>
                </article>
            </div>
        </div>

        <div>
            <section class="call-to-action">
                <section class="info container-huge hidden-scroll">
                    <p class="text-danger">Join our mailing list today</p>
                    <h3 class="">Insider offers & flash sales in your inbox every week</h3>
                    <div class="form ">
                        <input type="email" placeholder="Insert your email....*" class="">
                        <button class="sub btn btn-primary "> Subscribe</button>
                    </div>
                    <p class="gray">Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet,
                        consectetur
                        adipiscing elit sed porttitor lectus.
                    </p>
                </section>
            </section>
        </div>
    </div>
</template>

<style lang=scss scoped>
@use '../style/partials/variables.scss' as *;

figure {
    width: 50%;
    height: 1000px;
    position: relative;
    top: -50px;
    background-image: linear-gradient(to top, rgba(0, 0, 0, 0.63), transparent),
        url('../images/service15-2x.jpg');
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
}

.caption {
    width: 40%;
    padding: 8rem;

    .link {
        color: #4154ff;
        font-size: 2rem;
        text-align: start;
    }

    .title {
        font-size: 4rem;
    }

    .text {
        font-size: 1.5rem;
    }

    .bottone {
        width: 50%;
    }
}

.playlist {
    margin-bottom: 4rem;
}

.wrapper {
    width: 100%;
    display: flex;
    justify-content: space-between;
}

.video-container {
    width: 30%;
    display: flex;
    flex-direction: column;
}

.video {
    width: 100%;
    height: 300px;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
}

h2,
h3 {
    color: black;
}

.call-to-action {
    width: 100%;
    color: white;
    height: 1000px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    background-image: linear-gradient(to right, black, black, black, transparent, transparent),
        url('https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/banner1@2x.jpg');

    .info {
        padding: 10rem 0;

        p {
            color: $red;
            font-size: 2rem;
            width: 65%;
        }

        h3 {
            width: 60%;
            color: white;
            font-size: 4rem;
        }
    }
}

.form {
    display: flex;
    margin-bottom: 2rem;

    input {
        width: 40%;
        padding: 1rem;
        border-radius: 50px;
        margin-right: 2rem;
        font-size: 1.2rem;
    }

    button {
        width: 20%;
        font-weight: bold;
        font-size: 1.2rem;
    }
}


button.bg-red {
    background-color: red;
    width: fit-content;
    font-size: 1.2rem;
    font-weight: bold;
    &:hover {
        background-color: rgb(255, 101, 101);
    }
}

a {
    text-decoration: none;
}

/**  Animations  */


.hidden-scroll {
    opacity: 0;
    visibility: hidden;
    transition: opacity 1.5s ease, transform 1.5s ease;
}

.visible-scroll {
    opacity: 1;
    visibility: visible;
}

</style>