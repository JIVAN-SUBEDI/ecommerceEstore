<template>
    <div class="container">
        <div class="main_container">
            <div class="left">
                <h1>Get Our</h1>
                <h1>Latest Offers News</h1>
                <p>subscribe newsletter</p>
            </div>
            <div class="right">
                <input type="text" placeholder="Your email here..">
                <button>Subscribe</button>
            </div>
        </div>
    </div>
</template>
<script>
export default{
    name:"newsletterVue"
}
</script>
<style scoped>
.container{
    height: calc(100vh - 80px);
    display: flex;
    justify-content: center;
    align-items: center;

}
.main_container{
    display: flex;
    justify-content: space-around;
    background: #c8ebff;
    align-items: center;
    height: 80%;
    width: 90%;
    border-radius: 5px;
}
.right{
    width: 40%;
    position: relative;
}
.right input{
    
    width: 100%;
    height: 55px;
    border-radius: 27.5px;
    border:none;
    padding: 0 32% 0 1.5rem;
    outline: none;
}
.right button{
    width: 30%;
    height: 55px;
    border-radius: 27.5px;
    position: absolute;
    right: 0;
    border: none;
    background:#1f79ff ;
    font-size: 1rem;
    color: white;

}
.left h1{
    font-weight: 500;
    font-size: 2.5rem;
}

</style>