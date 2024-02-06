<template>
    <div class="orderContainer">
        <h3>My Orders</h3>
        <div class="filter">
            <p>Show:</p>
            <select name="" id="">
                <option value="">Last 5 Days</option>
                <option value="">Last 5 Days</option>
                <option value="">Last 5 Days</option>
                <option value="">Last 5 Days</option>
                <option value="">Last 5 Days</option>
            </select>
        </div>
        <div class="orders">
            <div class="orderTop">
                <p>order #4540</p>
                <a href="">View</a>
            </div>
            <div class="orderMain">
                <div class="image_container">

                    <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8cHJvZHVjdHxlbnwwfHwwfHx8MA%3D%3D" alt="">
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt, commodi ut! Laboriosam consectetur quasi explicabo.</p>
                </div>
                <p >Qty:1</p>
                <p class="badge badge-success">Delivered</p>
                <p>Delivered on 6 nov, 2024</p>
            </div>

        </div>
    </div>
</template>
<script>
export default{
    name:"orderPage"
}
</script>
<style scoped>
.orderContainer{
    height:100vh;
    padding: 1.5rem;
    overflow: auto;
    
}
h3{
    font-weight: 500;
}
.filter{
    height: 100px;
    background: #f2f2f2;
    display: flex;
    align-items: center;
    padding: 0 2rem;
}
.filter select{
    margin-left: 1.5rem;
    height: 45px;
    width: 200px;
    outline:none;
    border:1px solid #929291;
    border-radius: 5px;
}
.orders{
    margin-top: 1rem;
    height: 150px;
    padding: 1.5rem;
    background: #f2f2f2;
    /* display:flex;
    align-items: center;
    justify-content: space-between;*/
} 
.orderTop{
    height: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #929291;

}
.orderTop a{
    text-decoration: none;
}
.orderMain{
    height: calc(150px - 44px);
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.image_container{
    width: 40%;
    display: flex;
    height: 100%;
    align-items: center;
    
}
.image_container img{
    height: 95px;
    width: 95px;
}
.image_container p{
    font-size: 0.9rem;
    margin-left: 1.5rem;
    overflow: hidden;
text-overflow: ellipsis;
display: -webkit-box;
-webkit-line-clamp: 3;
-webkit-box-orient: vertical;
}
.badge-success{
    background: green;
    color: white;
}
.badge-warning{
    background: yellow;
    color: white;
}
.badge{
    padding: 0.5rem 1rem;
    border-radius: 5px;
}
</style>