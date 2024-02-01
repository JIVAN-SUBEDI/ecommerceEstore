<template>
  <div class="container">
    <div class="top">
      <h1>Shop by Category</h1>
      <div class="navigation">
        <a><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg></a>
        <a><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg></a>
      </div>
    </div>
    <swiper
    :slides-per-view="1"
    :space-between="50"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    :modules="modules"
    :loop="true"
    :autoplay="{
      delay:7000,
    
    }"
  >
    <swiper-slide>  <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div></swiper-slide>
    <swiper-slide>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
    </swiper-slide>
  </swiper>
    <!-- <div class="sliderContainer">
    
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
      <div class="slide">
        <img src="../../assets/category.png" alt="">
        <div class="details">
          <p>Women Wear</p>
          <a href="#">Shop Now</a>
        </div>
      </div>
    </div> -->
  </div>
</template>

<script>

 // Import Swiper Vue.js components
 import { Swiper, SwiperSlide } from 'swiper/vue';
 import {AutoPlay} from 'swiper';


// Import Swiper styles
import 'swiper/css';

export default {
  name: "categoryVue",
  components:{
    Swiper,
      SwiperSlide,
    
     
  },
  setup(){
    const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules:[AutoPlay]
      };
  }

};
</script>
<style scoped>
.sliderContainer{ 
  margin-top: 1.5rem;
  width: 100%;
  border: 1px solid red;
  display:flex;

  
}

.top{
  display: flex;
  justify-content: space-between;
}
.navigation{
  display: flex;
}
.navigation svg{
  width: 15px;
  height: 15px;
  fill: #929191;
}
.navigation a{
  width: 30px;
  height: 30px;
  margin-right: 0.5rem;

}
.slide{
    width: 300px;
  height: 200px;
  
  display: flex;
  background-color: #f2f2f2;
  border-radius: 5px;
}
.slide img{
  width: 50%;

}
.details{
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
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
   
}
.details p{
  font-size: 1.1rem;
  font-weight: 600;
}
</style>
