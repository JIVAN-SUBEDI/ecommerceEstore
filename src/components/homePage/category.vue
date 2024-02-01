<template>
  <div class="container">
    <div class="top">
      <h1>Shop by Category</h1>
      <div class="navigation">
        <a @Click="goToPrev()"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg></a>
        <a @Click="goToNext()"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg></a>
      </div>
    </div>
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <!-- Your slides go here -->
        <div class="swiper-slide">
          <img src="../../assets/category.png" alt="" />
          <div class="details">
            <p>Women Wear</p>
            <a href="#">Shop Now</a>
          </div>
        </div>
        <div class="swiper-slide"><img src="../../assets/category.png" alt="" />
          <div class="details">
            <p>Women Wear</p>
            <a href="#">Shop Now</a>
          </div></div>
        <div class="swiper-slide"><img src="../../assets/category.png" alt="" />
          <div class="details">
            <p>Women Wear</p>
            <a href="#">Shop Now</a>
          </div>
        </div>
        <div class="swiper-slide"><img src="../../assets/category.png" alt="" />
          <div class="details">
            <p>Women Wear</p>
            <a href="#">Shop Now</a>
          </div>
        </div>
        <div class="swiper-slide"><img src="../../assets/category.png" alt="" />
          <div class="details">
            <p>Women Wear</p>
            <a href="#">Shop Now</a>
          </div>
        </div>
        <div class="swiper-slide"><img src="../../assets/category.png" alt="" />
          <div class="details">
            <p>Women Wear</p>
            <a href="#">Shop Now</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper, { Navigation, Pagination, Autoplay } from "swiper";

// Import Swiper styles
import "swiper/swiper-bundle.css";

// Install Swiper modules
Swiper.use([Navigation, Pagination, Autoplay]);

export default {
  name: "categoryVue",
  data(){
    return{mySwiper:null}
  },
  mounted() {
    // Initialize Swiper with autoplay
    this.mySwiper = new Swiper(".swiper-container", {
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
      },
      slidesPerView: 3.1,

      autoplay: {
        delay: 1000, // Set the autoplay delay in milliseconds (e.g., 5000ms or 5s)
        disableOnInteraction: false, // Autoplay continues even when the user interacts with the slider
      },
    });
  },
  methods:{
    goToPrev() {
        console.log("hello");
      if (this.mySwiper) {
        this.mySwiper.slidePrev();
      }
    },
    goToNext() {
      if (this.mySwiper) {
        this.mySwiper.slideNext();
      }
    },
  }
};
</script>

<style scoped>
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
  cursor: pointer;

}
.swiper-container {
  width: 100%;
  height: 100%;
  overflow: hidden;
  margin-top: 2rem;
}
.swiper-slide {
  text-align: center;
  font-size: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.swiper-container .swipper-wrapper{
    width:100%;
}
.swiper-slide{
    /* width: 250px; */
  height: 200px;

  display: flex;
  background-color: #f2f2f2;
  border-radius: 5px;
  margin-right:1rem;
}
.swiper-slide img{
  width: 50%;
  height: 100%;
  object-fit: contain;

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
