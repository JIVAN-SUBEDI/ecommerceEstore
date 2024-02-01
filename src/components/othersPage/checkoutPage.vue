<template>
    <headerVue/>
    <navbarVue/>
    <div class="checkout_container">
        <div class="checkout_main">
        <div class="form">
            <h3>Billing Details</h3>
            <div class="row">
                <div class="col">

                    <label for="">First Name <span class="text-danger">*</span></label>
                    <input type="text" name="" id="" placeholder="First name">
                </div>
                <div class="col">
                    <label for="">Last Name <span class="text-danger">*</span></label>
                    <input type="text" name="" id="" placeholder="First name">
                </div>
            </div>
            <div class="row">
                <div class="col">
                        <label for="">Phone Number <span class="text-danger">*</span></label>
                    <input type="text" name="" id="" placeholder="Phone number">
                </div>
                <div class="col">
                    <label for="">Email Address</label>
                    <input type="text" name="" id="" placeholder="Email Address">
                </div>
            </div>
            <div class="col">
                <label for="">Country</label>
                <select name="" id="">
                    <option value="">Select Country</option>
                    <option value="test">test</option>
                </select>
            </div>
            <div class="col">
                <label for="">Addressline 1</label>
                <input type="text" name="" id="" placeholder="Addressline 1">
            </div>
            <div class="col">
                <label for="">Addressline 2</label>
                <input type="text" name="" id="" placeholder="Addressline 2">
            </div>
            <div class="col">
                <label for="">Town/City</label>
                <input type="text" name="" id="" placeholder="Town/City">
            </div>
            <div class="col">
                <label for="">Postcode/Zipcode</label>
                <input type="text" name="" id="" placeholder="Postcode/Zipcode">
            </div>
            <h3>Shipping Details</h3>
            <div >
                <input type="checkbox" name="" id="">
                <label for="">Same As Billing Address</label>
            </div>
            <div class="col">
                <label for="">Country</label>
                <select name="" id="">
                    <option value="">Select Country</option>
                    <option value="test">test</option>
                </select>
            </div>
            <div class="col">
                <label for="">Addressline 1</label>
                <input type="text" name="" id="" placeholder="Addressline 1">
            </div>
            <div class="col">
                <label for="">Addressline 2</label>
                <input type="text" name="" id="" placeholder="Addressline 2">
            </div>
            <div class="col">
                <label for="">Town/City</label>
                <input type="text" name="" id="" placeholder="Town/City">
            </div>
            <div class="col">
                <label for="">Postcode/Zipcode</label>
                <input type="text" name="" id="" placeholder="Postcode/Zipcode">
            </div>
        </div>
        <div class="details">
            <h3>
                Your Orders
            </h3>
            <table>
                <tr>
                    <td class="w-50">Product</td>
                    <td class="w-25"></td>
                    <td class="w-25">Price</td>
                </tr>
                <tr>
                    <td class="w-50">Hoodie</td>
                    <td class="w-25">x2</td>
                    <td class="w-25">$50</td>
                </tr>
                <tr>
                    <td class="w-50">Hoodie</td>
                    <td class="w-25">x2</td>
                    <td class="w-25">$50</td>
                </tr>
                <tr>
                    <td class="w-50">Hoodie</td>
                    <td class="w-25">x2</td>
                    <td class="w-25">$50</td>
                </tr>
                <tr>
                    <td class="w-50">Subtotal</td>
                    <td class="w-25"></td>
                    <td class="w-25">$500</td>
                </tr>
                <tr>
                    <td class="w-50">Shipping</td>
                    <td class="w-25"></td>
                    <td class="w-25">$500</td>
                </tr>
                <tr>
                    <td class="w-50">Discount</td>
                    <td class="w-25"></td>
                    <td class="w-25">-$500</td>
                </tr>
                <tr>
                    <td class="w-50">Total</td>
                    <td class="w-25"></td>
                    <td class="w-25">$500</td>
                </tr>
            </table>
            <div class="coupon">

                <p>Have a Coupon ?</p>
                <input type="text" >
                <button>Apply</button>
            </div>
            <div class="paymentMethod">
                <h3>Payment Method</h3>
                <div>
                    <input type="radio" name="payment" value="card"><span>Card</span>
                </div>
                <div>

                    <input type="radio" name="payment" value="paypal"><span>Paypal</span>
                </div>
                <div>

                    <input type="radio" name="payment" value="cash"><span>Cash on Delivery</span>
                </div>

            </div>
            <div class="payContainer">

                <button class="pay">Order</button>
            </div>
        </div>
        </div>
    </div>
    <footerVue/>    
</template>
<script>
import headerVue from '../header.vue';
import navbarVue from '../navbar.vue';
import footerVue from '../footer.vue';
export default{
    name:"checkoutPage",
    components:{
        navbarVue,headerVue,footerVue
    }
}
</script>
<style scoped>
.text-danger{
    color: red;
}
h3{
    font-weight: 500;
    margin-top: 1rem;
}
.checkout_container{
    margin: 2rem 0;
    width:100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.checkout_main{
    width: 85%;
    display: grid;
    grid-template-columns: 4fr 1.5fr;
    grid-gap: 2rem;
}

.row{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 1rem;

}
.col{
    display: grid;
    grid-template-rows: 1fr 1fr;
}
.col input, .col select{
    height: 40px;
    border: 1px solid #929291;
    outline: none;
    padding: 0 1rem;
    border-radius: 5px;
}
.col label{
    margin-top: 1rem;
    margin-bottom: .5rem;
}
.form input[type="checkbox"]{
    margin-right: 1rem;
    margin-top: 1rem;
}
.details{
    background: #f2f2f2;
    border-radius: 5px;
    padding: 1rem;
}
.details h3{
    width: 100%;
    color: #1f79ff;
    border-bottom: 1px solid #929291;
}
td{
    height: 40px;
    border-bottom: 1px solid #929291;
    color: black;
    
}
.w-50{
    width: 50%;
}
.w-25{
    width: 25%;
}
table{
    width: 100%;
    margin-top: 1.5rem;
}

.details span{
    margin-left: 1rem;
    color: black;
}
.paymentMethod h3{
    margin-bottom: 1rem;
 
}
.paymentMethod div{
    height: 40px;
}
.details p{
    color: #1f79ff;
}
.pay{
    height: 45px;
    padding: 0 1rem;
    font-size: 1rem;
    background: #1f79ff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
.payContainer{
    width: 100%;
    display: flex;
    justify-content: center;
    
}
.coupon{
    /* display: flex;
    flex-direction: column;
    align-items: center; */
    width: 100%;
}
.coupon input{
    width:100%;
    height: 40px;
    border-radius: 20px;
    border: 1px solid #929291;
    
}
.coupon button{
    height: 45px;
    padding: 0 1rem;
    font-size: 1rem;
    background: #1f79ff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 1rem;
}
</style>