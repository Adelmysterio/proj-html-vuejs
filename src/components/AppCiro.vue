<script>
import { faImages } from '@fortawesome/free-solid-svg-icons';

export default {
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
            ArticleCard: [
                {
                    id: 0,
                    icon: 'fas fa-stopwatch-20',
                    title: 'Team training',
                    ywtitle: 'Find a partner',
                    text: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.',
                    link: 'Find a partner >',
                },
                {
                    id: 1,
                    icon: 'fas fa-dumbbell',
                    title: 'Crossfit workout',
                    ywtitle: 'Push your limits',
                    text: 'Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.',
                    link: 'Learn about Crossfit >',
                },
                {
                    id: 2,
                    icon: 'fas fa-hotdog',
                    title: 'Weight loss plant',
                    ywtitle: 'Shed those pounds',
                    text: 'At laoreet senectus volutpat diam vel sed sed amet pellentesque. Lobortis ut aliquam risus purus. A tellus ut etiam.',
                    link: 'Schedule a workout >',
                },

            ]
        };
    }
}
</script>

<template>

    <div class="container-fluid">
        <div class="container-huge">
            <div class="row">
                <div class="workouts d-flex w-100">
                    <img src="../images/service15-2x.jpg" alt="service15" id="service" class="col-6">
                    <article class="artup d-flex flex-column" v-for="item in ArticleData">
                        <p class="link">{{ item.link }}</p>
                        <p class="title">{{ item.title }}</p>
                        <p class="text"> {{ item.text }}</p>
                        <button class="bottone btn btn-danger text-light">Visit my YouTube channel</button>
                    </article>
                </div>
                <div class="playlists d-flex col-5 w-100 flex-column">
                    <div class="video-up">
                        <h2>Feautred playlists</h2>
                    </div>
                    <div class="video-container">
                        <article class="video" v-for="item in CardData" :key="item.id">
                            <img :src="item.image" alt="" class="test">
                            <h3>{{ item.title }}</h3>
                            <a :href="item.link">{{ item.link }}</a>
                        </article>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <section class="up">
                <section class="into-up">
                    <h3 class="text-danger">Join our mailing list today</h3>
                    <h1>Insider offers & flash sales in your inbox every week</h1>
                    <div class="form">
                        <input type="email" placeholder="insert your email....*">
                        <button class="sub btn btn-primary"> Subscribe</button>
                    </div>
                    <p>Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet, consectetur
                        adipiscing elit sed porttitor lectus.</p>
                </section>
            </section>
            <section class="low">
                <article v-for="item in ArticleCard" :key="item.id">
                    <i :class="item.icon" id="mammt"></i>
                    <p>{{ item.title }}</p>
                    <p class="text-warning">{{ item.ywtitle }}</p>
                    <p>{{ item.text }}</p>
                    <a :href="item.link"></a>
                </article>
            </section>
        </div>
    </div>
</template>

<style lang=scss scoped>

.low {
    display: flex;
    width: 100%;
    background-color: #060607;
    color: white;

    article {
        width: calc(80% / 3);
        font-weight: bold;
        text-align: center;
        padding: 3rem;
        align-items: center;
        justify-content: center;
        border: 3px solid #4154ff;
        margin: 2rem;
    }
}

.video-container {
    width: 100%;
    display: flex;
}

.video {
    width: 100%;

    img {
        width: 100%;
    }
}

.up {
    width: 100%;
    color: white;
    height: 700px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    background-image: url('https://avada.website/fitness/wp-content/uploads/sites/130/2019/11/banner1@2x.jpg');

    .into-up {
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin: 4rem;
        margin: 4rem;
        width: 40%;
        font-size: 2rem;
        font-weight: bold;

        .form {
            display: flex;
            align-items: center;
        }

        .sub {
            margin-left: 2rem;
            padding: 1rem;
            align-self: center;
            width: 30%;
        }

        p {
            font-size: 1.2rem;
            color: #98939f;
            padding: 1.5rem;
            font-weight: lighter;
        }
    }
}

#service {}

.artup {
    justify-content: center;
    align-self: center;
    width: 40%;
    padding: 3rem;

    .link {
        color: #4154ff;
        font-size: 1.3rem;
        text-align: start;
    }

    .title {
        font-weight: bold;
        font-size: 2rem;
    }

    .text {
        font-size: 1.1rem;
    }

    .bottone {
        width: 50%;
    }
}
</style>