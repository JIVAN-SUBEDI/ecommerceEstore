<template>
    <div>

        <div class="productContainer">
            <cardVue v-for="product in products" :key="product.name" :details="product"/>
        </div>
        <ul class="pagination">
            <li><button ><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg></button></li>
            <li><button class="active">1</button></li>
            <li><button >2</button></li>
            <li><button >3</button></li>
            <li><button >4</button></li>
            <li><button >5</button></li>
            <li><button><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg></button></li>
        </ul>
    </div>
    </template>
<script>
import cardVue from '../card.vue'
import {ref} from 'vue';
export default{
    name:"productVue",

    components:{cardVue},
    setup(){
        const products = ref([
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
<style scoped>
.productContainer{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
}
.pagination{
    display:flex;
    align-items: center;
    justify-content: center;
    padding: 2rem;
    width: 100%;

}
.pagination li{
    list-style: none;
    margin-left: 1rem;
}
.pagination button{
    text-decoration: none;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    border: 1px solid #929291;
    color: #929291;
    background: transparent;
    font-weight: 500;
    cursor:pointer;
    display: flex;
    justify-content: center;
    align-items: center;

}
.pagination button:hover, .pagination button:hover svg{
    border: 1px solid #1f79ff;
    background: #1f79ff;
    color: white;
    fill: white;
   
}
.pagination svg{
    width:15px;
    height: 15px;
    fill: #929291;
}
.pagination .active{
    border: 1px solid #1f79ff;
    background: #1f79ff;
    color: white;
}
</style>