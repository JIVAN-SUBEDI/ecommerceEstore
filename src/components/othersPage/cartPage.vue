<template>
    <headerVue/>
    <navbarVue/>
  <div class="cart_container">
    <div class="header">
      <div class="check">
   
      </div>
      <h3 class="price">Product</h3>
      <h3 class="price">Price</h3>
      <h3 class="price">Quantity</h3>
      <h3 class="price">Total</h3>
    </div>
    <div class="cartItems">
      <div class="item" v-for="product in products.items" :key="product.id">
        <div class="check">
          <input type="checkbox" @change="checkbox(product.id, index)"  />
        </div>
        <div class="product">
          <img :src="product.img" alt="" />
          <p>{{ product.name }}</p>
        </div>
        <div class="price">${{ product.price }}</div>
        <div class="quantity">
          <input type="text" :value="product.quantity" disabled />
          <div class="controls">
            <button @click="plusValue(product.id)">+</button>
            <button @click="minusValue(product.id)">-</button>
          </div>
        </div>
        <div class="price">${{ product.totalPrice }}</div>
      </div>
    </div>
    <div class="header">
      <div></div>
      <h3></h3>
      <h3></h3>
      <h3 class="price">Subtotal</h3>
      <h3 class="price">${{ total.total }}</h3>
    </div>
    <div class="proceed">
        <button class="checkout">Proceed To Checkout</button>
    </div>
  </div>
  <footerVue/>
</template>
<script>
import { reactive } from "vue";
import headerVue from '../header.vue';
import footerVue from '../footer.vue';
import navbarVue from '../navbar.vue';
export default {
  name: "cartPage",
  components:{
    headerVue,footerVue,navbarVue
  },
  setup() {
    const checkId = reactive({
      items: [],
    });
    const total = reactive({
        total:0,
    });

    const products = reactive({
      items: [
        {
          id: 1,
          name: "Product 1",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 25.0,
          totalPrice: 25.0,
          quantity: 1,
        },
        {
          id: 2,
          name: "Product 2",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 30.0,
          totalPrice: 30.0,
          quantity: 1,
        },
        {
          id: 3,
          name: "Product 3",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 35.0,
          totalPrice: 35.0,
          quantity: 1,
        },
        {
          id: 4,
          name: "Product 4",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 40.0,
          totalPrice: 40.0,
          quantity: 1,
        },
        {
          id: 5,
          name: "Product 5",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 45.0,
          totalPrice: 45.0,
          quantity: 1,
        },
        {
          id: 6,
          name: "Product 6",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 50.0,
          totalPrice: 50.0,
          quantity: 1,
        },
        {
          id: 7,
          name: "Product 7",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 55.0,
          totalPrice: 55.0,
          quantity: 1,
        },
        {
          id: 8,
          name: "Product 8",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 60.0,
          totalPrice: 60.0,
          quantity: 1,
        },
        {
          id: 9,
          name: "Product 9",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 65.0,
          totalPrice: 65.0,
          quantity: 1,
        },
        {
          id: 10,
          name: "Product 10",
          img: "https://preview.colorlib.com/theme/estore/assets/img/categori/product2.png",
          price: 70.0,
          totalPrice: 70.0,
          quantity: 1,
        },
      ],
    });

    const plusValue = (id) => {
      const change = products.items.find((obj) => obj.id === id);
      if (change) {
        change.quantity += 1;
        change.totalPrice = change.quantity * change.price;
        updateTotal();
      }
    };
    const minusValue = (id) => {
      const change = products.items.find((obj) => obj.id === id);
      if (change) {
        if (change.quantity > 1) {
          change.quantity -= 1;
          change.totalPrice = change.quantity * change.price;
          updateTotal();
        }

      }
    };
    const checkbox = (id) => {
      const index = checkId.items.indexOf(id);
      if (index !== -1) {
        checkId.items.splice(index, 1);
      } else {
        checkId.items.push(id);
      }
      updateTotal();
    };
    const updateTotal = () => {
        let totalprice =0;
      checkId.items.forEach((element) => {

        const change = products.items.find((obj) => obj.id === element);
        if (change) {
            totalprice += change.totalPrice;

        }
      });
      total.total = totalprice;
    };
 
    return { products, plusValue, minusValue, checkbox,total };
  },
};
</script>
<style scoped>
.cart_container {
  width: 100%;
  padding: 1.5rem;
  background: #f2f2f2;
}
.header {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr 2fr 1fr;
  padding: 0.5rem 0;
  border-bottom: 1px solid #929291;
}
.item {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr 2fr 1fr;
  padding: 0.5rem 0;
  border-bottom: 1px solid #929291;
  height: 100px;
}
h3 {
  font-weight: 400;
  color: #929291;
}
input[type="checkbox"] {
  width: 20px;
  height: 20px;
}
.check {
  display: flex;
  justify-content: center;
  align-items: center;
}
.price {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.product {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  /* height: 100px; */
  margin: -1rem;
}
.product img {
  height: 90px;
  width: 90px;
  object-fit: cover;
}
.quantity {
  display: flex;
  justify-content: center;
  align-items: center;
}
.quantity input {
  height: 50px;
  width: 50px;
  border: 1px solid #929291;
  text-align: center;
  font-size: 1.1rem;
  outline: none;
}
.controls {
  display: flex;
  flex-direction: column;
}
.controls button {
  width: 30px;
  height: 25px;
  background: transparent;
  border: 1px solid #929291;
  font-size: 1.1rem;
  color: #929291;
  cursor: pointer;
}
.controls button:first-child {
  border-left: none;
  border-bottom: none;
}
.controls button:last-child {
  border-left: none;
}
.proceed{
    display: flex;
    justify-content: flex-end;
    margin-top: 1.5rem;
}
.checkout{
    height: 50px;
    padding: 0 0.5rem;
    border-radius: 5px;
    border: none;
    background: #1f79ff;
    color: white;
    font-size: 1rem;
    cursor: pointer;
}
</style>
