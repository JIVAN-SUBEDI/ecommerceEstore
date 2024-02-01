<template>
  <headerVue/>
  <navbarVue/>
  <div class="confirm_container">
    <div class="column_container">
      <div class="message">
        Thank you. Your order has been received.
      </div>
      <div class="row_container">
        <div class="bg-light">
            <div>
          <h3>Order Info</h3>
            <table>
              <tr>
                <td class="w-50">Order Number</td>
                <td class="w-50">#0001</td>
              </tr>
              <tr>
                <td class="w-50">Date</td>
                <td class="w-50">23 jan, 2024</td>
              </tr>
              <tr>
                <td class="w-50">Total</td>
                <td class="w-50">$500</td>
              </tr>
              <tr>
                <td class="w-50">Payment Method</td>
                <td class="w-50">Cash On Delivery</td>
              </tr>
            </table>
          </div>
          <div>
            <h3>Shipping Address</h3>
            <table>
              <tr>
                <td class="w-50">Street</td>
                <td class="w-50">Buddha Subba path, Vijayput</td>
              </tr>
              <tr>
                <td class="w-50">City</td>
                <td class="w-50">Dharan</td>
              </tr>
              <tr>
                <td class="w-50">Country</td>
                <td class="w-50">Nepal</td>
              </tr>
              <tr>
                <td class="w-50">Post Code</td>
                <td class="w-50">5700</td>
              </tr>
            </table>
          </div>
        </div>
        <div class="bg-light">
            <h3>Billing Address</h3>
            <table>
              <tr>
                <td class="w-50">Street</td>
                <td class="w-50">Buddha Subba path, Vijayput</td>
              </tr>
              <tr>
                <td class="w-50">City</td>
                <td class="w-50">Dharan</td>
              </tr>
              <tr>
                <td class="w-50">Country</td>
                <td class="w-50">Nepal</td>
              </tr>
              <tr>
                <td class="w-50">Post Code</td>
                <td class="w-50">5700</td>
              </tr>
            </table>
        </div>

      </div>
      <div class="orderDetails bg-light">
        <h3>Order Details</h3>
        <table class="orderTable" >
            <tr>
                <th class="w-50">Product</th>
                <th class="w-25">Quantity</th>
                <th class="w-25">Total</th>
            </tr>
            <tr>
                <td class="w-50 text-center">Product 1</td>
                <td class="w-25 text-center">2</td>
                <td class="w-25 text-center">$200</td>
            </tr>
            <tr>
                <td class="w-50 text-center">Product 1</td>
                <td class="w-25 text-center">2</td>
                <td class="w-25 text-center">$200</td>
            </tr>
            <tr>
                <td class="w-50 text-center">Product 1</td>
                <td class="w-25 text-center">2</td>
                <td class="w-25 text-center">$200</td>
            </tr>
            <tr>
                <td class="w-50"></td>
                <td  class="w-25 text-center">Subtotal</td>
                <td class="w-25 text-center">$200</td>
            </tr>
            <tr>
                <td class="w-50"></td>
                <td  class="w-25 text-center">Shipping</td>
                <td class="w-25 text-center">$200</td>
            </tr>
            <tr>
                <td class="w-50"></td>
                <td  class="w-25 text-center">Total</td>
                <td class="w-25 text-center">$500</td>
            </tr>
        </table>
      </div>
    </div>
  </div>
  <footerVue/>
</template>
<script>
import headerVue from '../header.vue';
import footerVue from '../footer.vue';
import navbarVue from '../navbar.vue';

export default {
    name:"confirmationPage",
    components:{
      headerVue,footerVue,navbarVue
    }
};
</script>
<style scoped>
.confirm_container{
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 2rem 0;
}
.column_container{
    display: flex;
    flex-direction: column;
    align-items: center;

    width: 85%;
}
.row_container{
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 2rem;
}
.bg-light div{
    margin-top: 2rem;
}
.bg-light div:first-child{
    margin-top:0 ;
}
.bg-light{
    background: #f2f2f2;
    margin-top:2rem ;
    padding: 1.5rem;
    border-radius: 4px;
}
table{
    width:100%;
    
}
.orderTable, .orderTable th , .orderTable td{
    border: 1px solid #929291;
    border-collapse: collapse;
}
.orderTable th, .orderTable td{
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
}
tr{

    display: flex;
    justify-content: space-between;
}
tr td:last-child{
    color: #929291;
}
.w-50{
   width: 50%;
}
.w-25{
   width: 25%;
}
.w-75{
    width: 75%;
}
h3{
    font-weight: 500;
}
.orderDetails{
    width: 100%;
}
.text-center{
    text-align: center;
}

.message{
    color: #1f79ff;
}

</style>
