<script>
export default {
data() {
return {

}
}
}
</script>

<template>

<section class="buy-avada ">
    
  <div class="contenuto-banner d-flex  justify-content-center align-items-center flex-column">
      <h2 class="">"I've failed over and over again in my life. And that is why I succeded."</h2>
      <i class="fa-solid fa-stairs fa-rotate-by yellow" style="--fa-rotate-angle: 45deg;"></i>
      <p>Arcu auctor gravida nisl, congue sit nisi tincidunt eget proin. In lacinia lacus donec sed massa in ipsum eros, tristique. Gravida suspendisse etiam in iaculis</p>
      <input class="btn btn-primary" type="button" value="Buy Avada Today >">
  </div>

</section>

<section class="sponsors py-5">
  <div class="container">
    <div class="row">
      <div class="col-lg-3 col-md-6 col-sm-12 text-center mb-4">
        <img src="../images/sponsor-1-2x-200x103.png" alt="Yoga Studio Logo" class="img-fluid mb-3">
        <p><i class="fa-solid fa-stairs fa-rotate-by blue" style="--fa-rotate-angle: 45deg;"></i></p>
        <p>Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.</p>
        <a href="#">Visit Yoga Studio ></a>
      </div>
      <div class="col-lg-3 col-md-6 col-sm-12 text-center mb-4">
        <img src="../images/sponsor-2-2x-200x103.png" alt="Fitness Center Logo" class="img-fluid mb-3">
        <p><i class="fa-solid fa-stairs fa-rotate-by blue" style="--fa-rotate-angle: 45deg;"></i></p>
        <p>Feugiat etiam dui mauris pharetra mauris sed pharetra. Convallis sapien ornare cras faucibus nulla porta dui a.</p>
        <a href="#">Join Fitness Center ></a>
      </div>
      <div class="col-lg-3 col-md-6 col-sm-12 text-center mb-4">
        <img src="../images/sponsor-3-2x-200x103.png" alt="Fitness Club Logo" class="img-fluid mb-3">
        <p><i class="fa-solid fa-stairs fa-rotate-by blue" style="--fa-rotate-angle: 45deg;"></i></p>
        <p>Nisl at quam adipiscing montes, nec, adipiscing commodo aliquam tincidunt. Ligula in habitant et sagittis imperdiet.</p>
        <a href="#">Learn about FC ></a>
      </div>
      <div class="col-lg-3 col-md-6 col-sm-12 text-center mb-4">
        <img src="../images/sponsor-4-2x-200x103.png" alt="Power Gym Logo" class="img-fluid mb-3">
        <p><i class="fa-solid fa-stairs fa-rotate-by blue" style="--fa-rotate-angle: 45deg;"></i></p>
        <p>Proin in viverra maecenas et mattis ut nibh enim. Gravida ultricies mi porta lacus. Et posuere velit sed nec eleifend.</p>
        <a href="#">Visit Power Gym ></a>
      </div>
    </div>
  </div>
</section>

<section class="workout">


<section class="workout d-flex justify-content-center align-items-center text-center">

    <div class="contenuto-workout d-flex justify-content-center align-items-center flex-column">
       <input class="btn btn-primary" type="button" value="player">
        <h2>Crossfit workout of the day</h2>
        <h3>November 15th, 2019</h3>
        <a href="#">View all videos →</a>
    </div>

</section>


</section>



<div>
    <p>lorem*3</p>
</div>

</template>

<style lang="scss" scoped>

@use '../style/partials/_variables.scss' as *;

.buy-avada{
    background-color: red;
    height: 700px;
    background-image: url(../../src/images/banner2-2x.jpg);
    background-size: cover; 
    background-position: center; 
    background-repeat: no-repeat;
    color: white;

    .contenuto-banner{
      margin: 0 auto;
      text-align: center;
      padding: 10rem 25rem;
      background: rgba(0, 0, 0, 0.5);
      height: 100%;

      h2{
        font-size: 3rem;
        margin-bottom: 2rem;
      }

      p {
        color: rgba(214, 213, 216, 0.75);
        font-size: 1rem;
        margin-bottom: 2rem;
      }
    }
}

.sponsors {
  
  p {
    color: #666;
    font-size: 1rem;
  }
  
  a {
    color: black;
    text-decoration: none;
   
  }
}


.workout {
  

  height: 550px;
  background-image: url('../../src/images/banner14-2x.jpg'); 
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  color: white;
}

  .contenuto-workout {
    background: rgb(6,6,6);
    background: linear-gradient(90deg, rgba(6,6,6,0.4682247899159664) 0%, rgba(233,148,224,0.6979166666666667) 100%);
    padding: 2rem;
    width: 100%;
    height: 100%;
    text-align: center;

    h2 {
      font-size: 3rem;
      margin-bottom: 1rem;
    }

    h3 {
      font-size: 2rem;
      margin-bottom: 1rem;
      color: yellow;
    }

    a {
      color: white;
      font-size: 1rem;
    }
  }

  .yellow {
    color: yellow
  }

  .blue {
    color: blue;
  }

</style>
