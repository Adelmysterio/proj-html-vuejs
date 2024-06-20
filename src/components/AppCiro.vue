<script>
import { faImages } from '@fortawesome/free-solid-svg-icons';

export default {
data() {
return {
    CardData:[
                { id: 0, title: 'Thighs & glute workout', image: '../images/video2-2x.jpg', link: 'Increase your mobility' },
                { id: 1, title: 'Lift, firm & perk up', image: '../images/video7-2x.jpg', link: 'Feel young again' },
                { id: 2, title: 'Slim & trim your waist', image: '../images/video9-2x.jpg', link: 'Shed those extra pounds' },
                
            ],
    ArticleData:[
    { 
        id: 0, 
        title: 'The best health & fitness advice online', 
        text: 'Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper mauris, venenatis, leo integer sit pellentesque.' ,
        link: 'Tune up your workouts',
    },
    ]
        };
    }
}
</script>

<template>

<div class="container">
    <div class="row">
        <div class="workouts d-flex w-100">
            <img src="../images/service15-2x.jpg" alt="service15" id="service" class="col-6">
            <article class="artup d-flex flex-column"
            v-for="item in ArticleData"
            >
            <p class="link">{{ item.link }}</p>
            <p class="title">{{ item.title }}</p>
            <p class="text"> {{ item.text }}</p>
                <button class="bottone btn btn-danger text-light">Visit my YouTube channel</button>
            </article>
        </div>
        <div class="playlists d-flex col-5">
            <article
            v-for="item in CardData" :key="item.id"
            >
                <img :src="item.image" alt="" class="test">
                <h3>{{ item.title }}</h3>
                <a :href="item.link">{{ item.link }}</a>
            </article>
        </div>
    </div>
</div>

</template>

<style lang=
scss
scoped>
#service{
}
.artup{
    justify-content: center;
    align-self: center;
    width: 40%;
    padding: 3rem;
    .link{
        color: #4154ff;
        font-size: 1.3rem;
        text-align: start;
    }
    .title{
        font-weight: bold;
        font-size: 2rem;
    }
    .text{
        font-size: 1.1rem;
    }
    .bottone{
        width: 50%;
    }
}
</style>