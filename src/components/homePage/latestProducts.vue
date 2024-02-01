<template>
    <div class="container">
        <div class="top">

            <h1>Latest Products</h1>
            <ul>
                <li><a href="#">All</a></li>
                <li><a href="#">Featured</a></li>
                <li><a href="#">Offer</a></li>
            </ul>
        </div>
        <div class="main_container">
           <cardVue v-for="product in products" :key="product.name" :details="product" />
        </div>
    </div>
</template>
<script>
import { reactive } from 'vue';
import cardVue from '../card.vue';
export default{
    name:"latestproductVue",
    components:{cardVue
    },
    setup(){
        const products = reactive([
  {
    name: "Product 1",
    rating: 4,
    featured: 1,
    realPrice: 50.00,
    discountedPrice: 40.00,
    img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png"
  },
  {
    name: "Product 2",
    rating: 5,
    featured: 0,
    realPrice: 30.00,
    discountedPrice: 25.00,
    img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png"
  },
  {
    name: "Product 3",
    rating: 3,
    featured: 1,
    realPrice: 70.00,
    discountedPrice: 60.00,
    img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png"
  },
  {
    name: "Product 4",
    rating: 2,
    featured: 0,
    realPrice: 45.00,
    discountedPrice: 35.00,
    img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png"
  },
  {
    name: "Product 5",
    rating: 4,
    featured: 1,
    realPrice: 60.00,
    discountedPrice: 50.00,
    img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png"
  },
  {
    name: "Product 6",
    rating: 5,
    featured: 0,
    realPrice: 55.00,
    discountedPrice: 45.00,
    img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png"
  }
]);
return{
    products
}
    }


}
</script>
<style>
.container{
    padding: 2rem;
}
.container h1{
    font-weight: 500;

}
.top{
    display: flex;
    justify-content: space-between;
    padding: 0.5rem 0;
    border-bottom: 1px solid #929191;
}
.top ul{
    display: flex;
}
.top ul li{
    list-style: none;
    margin-right: 1.5rem;
    
}
.top ul li a{
    text-decoration: none;
    color: #929191;
}
.top ul li a:hover{
    color: #1f79ff;
}
.main_container{
    margin: 1.5rem 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

</style>