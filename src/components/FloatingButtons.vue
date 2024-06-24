<script>

</script>

<template>
    <div class="floating-buttons">
        <div class="icona-avada">
            <i class="fas fa-folder"></i>
            <p>Prebuilts</p>
        </div>
        <div class="icona-cart">
            <i class="fas fa-cart-shopping"></i>
            <p>Buy Now</p>
            
        </div>
    </div>
</template>

<style lang="scss" scoped>

@keyframes moveLeftRight {
    0% {
        transform: translateX(0px);
        opacity: 1;
    }
    50% {
        transform: translateX(70px);
        opacity: 1;
    }
    0% {
        transform: translateX(0px);
        opacity: 1;
    }
}

@keyframes moveRightLeft {
    0% {
        transform: translateX(0px);
        opacity: 1;
    }
    50% {
        transform: translateX(-70px);
        opacity: 1;
    }
    0% {
        transform: translateX(0);
        opacity: 1;
    }
}


.icona-avada, .icona-cart {
    position: fixed;
    width: 70px;
    height: 70px;
    background-color: white;
    right: 1%;
    top: 20%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border-radius: 20%;
    color: rgb(70, 70, 70);
    cursor: pointer;
    overflow: hidden; 
    z-index: 1;

    i {
        padding-top: 2px;
        font-size: 1.5rem;
        position: relative;
        transition: transform 0.4s cubic-bezier(.21, .6, .35, 1), opacity 0.4s cubic-bezier(.21, .6, .35, 1);
    }

    p {
        margin-bottom: 0;
        margin-top: 6px;
        font-weight: 600;
        font-size: .8rem;
    }
}

    .icona-avada:hover i{
        animation: moveLeftRight 0.4s forwards;
    }

    .icona-cart:hover i{
        animation: moveRightLeft 0.4s forwards;
    }

    .icona-cart {
    right: 1%;
    top: 29%;
    }


</style>