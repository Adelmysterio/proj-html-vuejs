<script>
export default {
data() {
    return {

        }
    },
}
</script>

<template>
    <div >
        <div class="card-container">
            <div class="card-wrapper">
                <div class="card-item container-huge">
                    <div class="card-content">
                        <i class="card-icon fas fa-stopwatch"></i>
                        <h4>
                            Team Training
                        </h4>
                        <h5>
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
                        <h5>
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
                        <h5>
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
    height: 500px;
    padding: 1rem;
    border: 3px solid #4154FF;
    border-radius: 10px;
    margin: 1rem;
    text-align: center;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: all .2s ease-in-out;
}

.card-item:hover {
    transform: scale(1.1); 
}

.card-item p{
    color: #D5D4D7;
    font-weight: 600;
    align-items: center;
    margin-bottom: 2rem;
}

.card-content{
    margin: 1rem;
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
    margin-top: 100px;
    padding-bottom: 100px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

h5{
    color: #FFF941;
}

</style>
