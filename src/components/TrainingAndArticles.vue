<script>
export default {
data() {
    return {

        }
    },
}
</script>

<template>
    <div>
        <div class="card-container">
            <div class="card-wrapper container-huge">
                <div class="card-item">
                    <div class="card-content">
                        <i class="card-icon fas fa-stopwatch"></i>
                        <h4>
                            Team Training
                        </h4>
                        <h5 class="mb-5">
                            Find a partner
                        </h5>
                        <p>
                            Lorem ipsum dolor, sit amet consectetur adipsicing elit. Eligendi, quasi qui ipsam earum laudantium nulla ducimus
                        </p>
                    </div>
                    <div>
                        <p class="card-link">
                            Find a Partner
                        </p>
                        <i class="card-arrow fas fa-angle-right"></i>
                    </div>
                </div>
                <div class="card-item">
                    <div class="card-content">
                        <i class="card-icon fas fa-dumbbell"></i>
                        <h4>
                            Team Training
                        </h4>
                        <h5 class="mb-5">
                            Find a partner
                        </h5>
                        <p>
                            Lorem ipsum dolor, sit amet consectetur adipsicing elit. Eligendi, quasi qui ipsam earum laudantium nulla ducimus
                        </p>
                    </div>
                    <div>
                        <p class="card-link">
                            Find a Partner
                        </p>
                        <i class="card-arrow fas fa-angle-right"></i>
                    </div>
                </div>
                <div class="card-item">
                    <div class="card-content">
                        <i class="card-icon fas fa-weight-scale"></i>
                        <h4>
                            Team Training
                        </h4>
                        <h5 class="mb-5">
                            Find a partner
                        </h5>
                        <p>
                            Lorem ipsum dolor, sit amet consectetur adipsicing elit. Eligendi, quasi qui ipsam earum laudantium nulla ducimus
                        </p>
                    </div>
                    <div>
                        <p class="card-link">
                            Find a Partner
                        </p>
                        <i class="card-arrow fas fa-angle-right"></i>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="container-huge">
        <div class="contenitore">
            <div class="articles-links">
                <h2>Latest article</h2>
                <div class="articles-readAll">
                    <a href="#" class="read-more">
                        Read all articles
                    </a>
                    <i class="fas fa-angle-right"></i>
                </div>
            </div>
            <div class="articles">
                <article>
                    <img src="../images/blog4-2x-400x258.jpg">
                    <h3>
                        The best protein shake
                    </h3>
                    <p>
                        Published On: November 26th, 2019 | 2 Comments
                    </p>
                </article>
                <article>
                    <img src="../images/blog1-2x-400x258.jpg">
                    <h3>
                        Ultimate Cardio Workout
                    </h3>
                    <p>
                        Published On: November 26th, 2019 | 0 Comments
                    </p>
                </article>
                <article>
                    <img src="../images/blog3-2x-400x258.jpg">
                    <h3>
                        New Juices Available
                    </h3>
                    <p>
                        Published On: November 26th, 2019 | 0 Comments
                    </p>
                </article>
            </div>
            
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../style/general.scss';

.card-container{
    background-color: #060607;
    width: 100%;
    
}

.card-item{
    max-width: 30%;
    min-width: 250px;
    height: 700px;
    padding: 7rem 2rem;
    border: 3px solid #4154FF;
    border-radius: 10px;
    text-align: center;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: all .2s ease-in-out;
    h4,
    h5 {
        font-size: 2rem;
        margin-bottom: .5rem;
        font-weight: bold;
    }
}

.card-item:hover {
    transform: scale(1.1); 
}

.card-item p{
    font-size: 1.2rem;
    color: #D5D4D7;
    font-weight: 600;
    align-items: center;
    margin-bottom: 2rem;
}

.card-icon{
    font-size: 4rem;
    margin-bottom: 2rem;
}

.card-link{
    display: inline-block;
    color: white;
}

.card-arrow{
    margin-left: .3rem;
    font-size: .8rem;
    font-weight: 600;
}

.card-wrapper{
   padding: 3rem 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

h5{
    color: #FFF941;
}
///////////////////////////////////////////////////////////////////////

.contenitore {
    color: black;
    padding: 8rem 0;
}

.articles-container{
    width: 100%;
    background-color: #f8f8f8;
    display: flex;
    justify-content: center;
    height: 60vh;
    padding: 100px;
}

.articles-links{
    display: flex;
    justify-content: space-between;
    padding-bottom: .6rem;
}

.articles-readAll {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: #000;
    transition: color 0.3s;
}
.articles-readAll a{
    text-decoration: none;
    color: inherit;
}


.articles-readAll:hover{
    color:#4154FF;
    
}

.articles{
    display: flex;
    justify-content: space-between;
}

article{
    width: 30%;
    display: flex;
    flex-direction: column;
}

article img{
    width: 100%;
    padding-bottom: 1rem;
}
</style>
