<script>
import axios from 'axios';
export default {

    data() {
        return {
            events: []
        };
    },
    methods: {
        getEvents() {

            axios.get('http://152.89.170.170:3000/events/fitness')
                .then((response) => {
                    // handle success
                    console.log(response.data);
                    this.events = response.data;
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                })
                .finally(function () {
                    // always executed
                });

        },

    },
    created() {
        this.getEvents();

    }
};
</script>

<template>
    <div class="bg-gradient">
        <div class="wrapper container-huge">
            <h2>Sign-Up Now! For the next fitness events!</h2>
            <div class="event" v-for="(event, index) in events" :key="index">
                <article :style="{ backgroundImage: 'url(' + event.image + ')' }" class="single-card">
                    <section>
                        <h3>{{ event.event_name }}</h3>
                        <p>{{ event.location }}</p>
                        <p>From {{ event.start_date }} to {{ event.end_date }}</p>
                        <p>{{ event.type }}</p>
                    </section>
                </article>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
.bg-gradient {
    background: linear-gradient(90deg, rgb(0, 0, 255), rgb(255, 0, 0)) !important;
}

.wrapper {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    padding: 0 0 10rem;
}

h2 {
    color: white;
    font-size: 4rem;
    margin: 0 auto;
    padding: 4rem 0;
}

.event {
    width: 30%;
}

article.single-card {
    width: 100%;
    height: 700px;
    margin-bottom: 3rem;
    transition: transform .35s;

    section {
        background: linear-gradient(to top, rgba(0, 0, 0, 0.699), transparent);
        padding: 90% 10% 20%;
        margin: 0;
    }

    h3 {
        font-size: 2rem;
        font-weight: bold;
        color: $yellow;
        margin-bottom: 4rem;
    }
}

article.single-card:hover{
    transform: scale(1.1);
}

</style>