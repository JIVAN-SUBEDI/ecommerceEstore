<template>
    <headerVue/>
    <navbarVue/>
  <div class="productDetails_container">
    <div class="productDetails">
      <div class="left">
        <div class="singleImage">
          <img :src="imageShow.image" />
        </div>
        <div class="imageList">
          <img
            :src="image"
            alt=""
            @click="changeImage(index)"
            v-for="(image, index) in product.imageList"
            :key="image"
          />
        </div>
      </div>
      <div class="right">
        <div class="title">
          {{ product.name }}
        </div>
        <div class="share_rating">
          <div class="rating">
            <svg
              :class="isActive(product, 1)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(product, 2)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(product, 3)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(product, 4)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(product, 5)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
          </div>
        </div>
        <p>Brand:{{ product.brand }}</p>
        <div class="price">
          <div class="discountedPrice">${{ product.discountedPrice }}</div>
          <div class="realPrice">${{ product.realPrice }}</div>
        </div>
        <div class="quantity">
          <button @click="minusValue" class="button">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
              <path
                d="M432 256c0 17.7-14.3 32-32 32L48 288c-17.7 0-32-14.3-32-32s14.3-32 32-32l352 0c17.7 0 32 14.3 32 32z"
              />
            </svg>
          </button>
          <input type="text" :value="quantity.qty" disabled />
          <button @click="plusValue" class="button">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
              <path
                d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32V224H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H192V432c0 17.7 14.3 32 32 32s32-14.3 32-32V288H400c17.7 0 32-14.3 32-32s-14.3-32-32-32H256V80z"
              />
            </svg>
          </button>
        </div>
        <div class="controls">
          <button class="button">Buy Now</button>
          <button class="button">Add to cart</button>
        </div>
      </div>
    </div>
    <div class="Reviews">
      <h3>Reviews</h3>
      <ul>
        <li v-for="review in review.visibleReview" :key="review.name">
          <div class="rating">
            <svg
              :class="isActive(review, 1)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(review, 2)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(review, 3)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(review, 4)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
            <svg
              :class="isActive(review, 5)"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 576 512"
            >
              <path
                d="M287.9 0c9.2 0 17.6 5.2 21.6 13.5l68.6 141.3 153.2 22.6c9 1.3 16.5 7.6 19.3 16.3s.5 18.1-5.9 24.5L433.6 328.4l26.2 155.6c1.5 9-2.2 18.1-9.7 23.5s-17.3 6-25.3 1.7l-137-73.2L151 509.1c-8.1 4.3-17.9 3.7-25.3-1.7s-11.2-14.5-9.7-23.5l26.2-155.6L31.1 218.2c-6.5-6.4-8.7-15.9-5.9-24.5s10.3-14.9 19.3-16.3l153.2-22.6L266.3 13.5C270.4 5.2 278.7 0 287.9 0zm0 79L235.4 187.2c-3.5 7.1-10.2 12.1-18.1 13.3L99 217.9 184.9 303c5.5 5.5 8.1 13.3 6.8 21L171.4 443.7l105.2-56.2c7.1-3.8 15.6-3.8 22.6 0l105.2 56.2L384.2 324.1c-1.3-7.7 1.2-15.5 6.8-21l85.9-85.1L358.6 200.5c-7.8-1.2-14.6-6.1-18.1-13.3L287.9 79z"
              />
            </svg>
          </div>
          <div>
            {{ review.message }}
          </div>
          <div class="name">{{ review.name }}</div>
        </li>
      </ul>
      <div class="loadMore">
        <button v-if="review.buttonShow" @click="loadMore" class="button">Load More</button>
      </div>
    </div>
    <div class="productDescription">
      <h3>Product Details</h3>
      <div class="description">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. A tempore,
        reiciendis, cum harum laborum eos est unde dolores quis veniam, fugiat
        placeat voluptatibus nemo ea libero sit recusandae quibusdam. Corporis
        beatae quos enim, tempora ad cupiditate, saepe commodi quas, suscipit
        quae voluptatum quaerat natus consequatur dolores. Non maiores incidunt
        officiis.
      </div>
    </div>
  </div>
  <footerVue/>
</template>
<script>
import { ref, reactive, onMounted } from "vue";
import headerVue from "../header.vue";
import footerVue from "../footer.vue";
import navbarVue from "../navbar.vue";
export default {
  name: "productDetails",
  components:{
    headerVue,footerVue,navbarVue
  },
  setup() {
    const review = reactive({
        visibleReview:[],
    reviewPerPage:5,
    firstIndex:1,
    buttonShow:false,
    reviews:[
      { message: "Great product!", name: "John", rating: 4 },
      { message: "Excellent service!", name: "Jane", rating: 5 },
      { message: "Could be better.", name: "Bob", rating: 2 },
      { message: "Awesome experience!", name: "Alice", rating: 4 },
      { message: "Fast delivery!", name: "Charlie", rating: 3 },
      { message: "Not satisfied.", name: "David", rating: 1 },
      { message: "Top-notch quality!", name: "Eva", rating: 5 },
      { message: "Quick response!", name: "Frank", rating: 4 },
      { message: "Poor customer service.", name: "Grace", rating: 1 },
      { message: "Impressive!", name: "Henry", rating: 5 },
      { message: "Average experience.", name: "Ivy", rating: 3 },
      { message: "Happy with the purchase!", name: "Jack", rating: 4 },
      { message: "Terrible product.", name: "Kelly", rating: 0 },
      { message: "Satisfied customer.", name: "Leo", rating: 4 },
      { message: "Prompt delivery!", name: "Mia", rating: 5 },
      { message: "Needs improvement.", name: "Nathan", rating: 2 },
      { message: "Highly recommended!", name: "Olivia", rating: 5 },
      { message: "Average quality.", name: "Peter", rating: 3 },
      { message: "Impatient customer support.", name: "Quinn", rating: 1 },
      { message: "Great value for money!", name: "Ryan", rating: 4 },
      { message: "Great value for money!", name: "jivan subedi", rating: 4 },
    ]});
    const quantity = reactive({qty:1});
    const product = ref({
      name: "Example Product",
      details: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
      rating: 4, // Rating between 1 to 5
      brand: "Example Brand",
      realPrice: 100.0,
      discountedPrice: 80.0,
      imageList: [
        "https://images.unsplash.com/photo-1511385348-a52b4a160dc2?q=80&w=1507&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        "https://thumbs.dreamstime.com/b/hands-computer-desk-using-laptop-rustic-wood-background-cup-tea-book-globe-glasses-53253551.jpg",
        "https://images.unsplash.com/photo-1511385348-a52b4a160dc2?q=80&w=1507&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        "https://images.unsplash.com/photo-1511385348-a52b4a160dc2?q=80&w=1507&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
      ],
    });
    const imageShow = reactive({
      image: product.value.imageList[0],
    });
    //to see the rating
    const isActive = (details, index) => {
      if (details.rating >= index) {
        return "active";
      } else {
        return "";
      }
    };
    //for changing the preview image
    const changeImage = (index) => {
      imageShow.image = product.value.imageList[index];
    };
    //to toggle the load more button
    const showLoadMoreButton = ()=>{
        if(review.reviewPerPage < review.reviews.length){
            review.buttonShow = true;
        }
        else{
            review.buttonShow = false;
        }
    }
    //to add five more visible review 
    const loadMore = ()=>{
        if(review.firstIndex <= review.reviews.length ){
            let value = review.reviews.length - review.firstIndex;
            
            let incr = value<5?(value+1):5;

            for(let i=review.firstIndex; i<(review.firstIndex+incr); i++){
                review.visibleReview.push(review.reviews[i-1]);
         
            }
            if(incr < 5){
                review.firstIndex += incr;
                review.buttonShow = false;
                
            }else{
                review.firstIndex += 5;

            }
        
            
        }else{
            review.buttonShow = false;
        }
    }
    //for increasing the quantity value by 1
    const plusValue = () => {

        quantity.qty +=1;
       
      
    }
    //for decreasing the quantity value by 1
    const minusValue = () => {
        if(quantity.qty > 1){

            quantity.qty-=1;
        }
     

      
    };
    //to load load more and load more button
    onMounted(()=>{
        showLoadMoreButton();
        loadMore();
    });
    return { product, isActive, imageShow, changeImage, review,showLoadMoreButton,loadMore,quantity,plusValue,minusValue };
  },
};
</script>
<style scoped>
.productDetails_container {
  width: 100%;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.productDetails {
  width: 85%;
  background: #f2f2f2;
  border-radius: 5px;
  display: flex;
  height: 400px;
}
.left {
  width: 40%;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.singleImage {
  height: 80%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.left img {
  width: 90%;
  height: 90%;
}
.left .imageList {
  width: 100%;
  height: 20%;
  overflow: hidden;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  object-fit: cover;
}
.imageList img {
  width: 20%;
  height: 90%;
  cursor: pointer;
}
.imageList img:hover {
  border: 1px solid red;
}
.right {
  width: 60%;
  padding: 1.5rem;
}
svg {
  width: 15px;
  height: 15px;
  fill: #929291;
}
svg.active {
  fill: orangered;
}
.rating {
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}
.right p {
  font-size: 0.8rem;
  color: #1f79ff;
}
.discountedPrice {
  margin-top: 1rem;
  font-size: 1.5rem;
}
.realPrice {
  color: red;
  text-decoration: line-through;
  font-size: 1.5rem;
}
.quantity input,
button {
  height: 45px;
  padding: 0 1rem;
  border: 1px solid #929291;
  margin-top: 1rem;
}

input {
  width: 50px;
  font-size: 1.1rem;
}
.quantity button {
  border: 1px solid #1f79ff;
  background: #1f79ff;
  cursor: pointer;
  font-size: 1.1rem;
}
.quantity button svg {
  fill: white;
}
.controls {
  margin-top: 1.5rem;
  width: 100%;
  display: flex;
  justify-content: space-between;
}
.controls button {
  width: 45%;
  background: #1f79ff;
  color: white;
  border: none;
  border-radius: 5px;
}
.Reviews {
  margin-top: 1.5rem;
  background: #f2f2f2;
  width: 85%;
  padding: 1.5rem;
  border-radius: 5px;
}
.Reviews ul {
  margin-top: 1rem;
  list-style: none;
}
.Reviews ul li {
  padding: 0.5rem;
  border-bottom: 1px solid #929291;
  /* border-top: 1px solid #929291; */
}
.Reviews .name {
  font-size: 0.8rem;
  color: #929291;
}
h3 {
  font-weight: 500;
  width: 100%;
  border-bottom: 1px solid #929291;
  /* margin: 1rem 0; */
}
.productDescription {
  margin-top: 1.5rem;
  width: 85%;
  background: #f2f2f2;
  padding: 1.5rem;
  border-radius: 5px;
}
.description {
  margin-top: 1rem;
}
.loadMore {
  width: 100%;
  display: flex;
  justify-content: center;
}
.loadMore button {
  background: #1f79ff;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  color: white;
  border-radius: 5px;
  border: 2px solid #1f79ff;
  cursor: pointer;
}
</style>
