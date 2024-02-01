<template>
    <div class="container">
        <img src="https://preview.colorlib.com/theme/estore/assets/img/hero/hero_man.png" alt="">
        <div class="details">
            <p>Discount 60% off</p>
            <h1>Winter Collection</h1>
            <p>Best collection form 2024</p>
            <a href="">Shop Now</a>
        </div>
    </div>
</template>
<script>
export default{
    name:"landingComp"
}
</script>
<style scoped>
.container{
    background: #c8ebff;
    height: calc(100vh - 110px);
    padding: 1.5rem 1.5rem 0 1.5rem;
    display: flex;
    justify-content: space-around;
    align-items: center;
    overflow:hidden ;

}
.container img{
    height: 100%;
    animation-name: animateImage;
    animation-delay: 1s;
    animation-fill-mode: forwards;
    animation-duration: 2s;
    animation-iteration-count:1 ;
}
.details a{
    text-decoration: none;
    width: 130px;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding:0.5rem 1rem;
    background: #1f79ff;
    color: white;
    border-radius: 10px;
    margin-top: 1.5rem;
    animation-name: animate;
    animation-delay: 1s;
    animation-fill-mode: forwards;
    animation-duration: 2s;
    animation-iteration-count:1 ;
    margin-left: 5rem;
    opacity: 0.5;

}
.details{

    width: 40%;
    height: 70%;
 
}
.details p:first-child{
    color: #1f79ff;

}
.details p{
    font-size: 1.8rem;
    font-style: italic;
    animation-name: animate;
    animation-delay: 1.3s;
    animation-fill-mode: forwards;
    animation-duration: 2s;
    animation-iteration-count:1 ;
    margin-left: 5rem;
    opacity: 0.5;
}
.details h1{
    font-size: 3.5rem;
    font-weight: 500;
    animation-name: animate;
    animation-delay: 1.6s;
    animation-fill-mode: forwards;
    animation-duration: 2s;
    animation-iteration-count:1 ;
    margin-left: 5rem;
    opacity: 0.5;

}
@keyframes animateImage {
    50%{
        transform: scale(1.05);
    }
    100%{
        transform: scale(1);

    }
}
@keyframes animate {
   
    100%{
      margin-left: 0;
      opacity: 1;

    }
}
</style>