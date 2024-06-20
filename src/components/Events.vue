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
    <div>
        <article v-for="(event, index) in events" :key="index" class="single-card">
            <img :src="event.image" :alt="event.event_name" class="" />
            <h3>{{ event.event_name }}</h3>
            <p>{{ event.location }}</p>
            <p>{{ event.start_date }} - {{ event.end_date }}</p>
            <p>{{ event.type }}</p>
        </article>
    </div>
</template>

<style lang="scss" scoped>
img {
    width: 100%;
}
</style>