<template>
    <div class="container">
        <div class="cards">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M50.7 58.5L0 160H208V32H93.7C75.5 32 58.9 42.3 50.7 58.5zM240 160H448L397.3 58.5C389.1 42.3 372.5 32 354.3 32H240V160zm208 32H0V416c0 35.3 28.7 64 64 64H384c35.3 0 64-28.7 64-64V192z"/></svg>
            <h3>Free Shipping</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita rerum voluptatibus eum, vel ducimus corrupti.</p>
        </div>
        <div class="cards">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path d="M64 64C28.7 64 0 92.7 0 128V384c0 35.3 28.7 64 64 64H512c35.3 0 64-28.7 64-64V128c0-35.3-28.7-64-64-64H64zm64 320H64V320c35.3 0 64 28.7 64 64zM64 192V128h64c0 35.3-28.7 64-64 64zM448 384c0-35.3 28.7-64 64-64v64H448zm64-192c-35.3 0-64-28.7-64-64h64v64zM288 160a96 96 0 1 1 0 192 96 96 0 1 1 0-192z"/></svg>
            <h3>Secured Payment System</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita rerum voluptatibus eum, vel ducimus corrupti.</p>
        </div>
        <div class="cards">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M0 80V229.5c0 17 6.7 33.3 18.7 45.3l176 176c25 25 65.5 25 90.5 0L418.7 317.3c25-25 25-65.5 0-90.5l-176-176c-12-12-28.3-18.7-45.3-18.7H48C21.5 32 0 53.5 0 80zm112 32a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"/></svg>
            <h3>Discounts</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita rerum voluptatibus eum, vel ducimus corrupti.</p>
        </div>
    </div>    
</template>
<script>
export default{
    name:"servicesVue"
}
</script>
<style scoped>
.container{
    height: calc(100vh - 80px);
    display: flex;
    justify-content: space-evenly;
    background: #f2f2f2;
    align-items: center;
    flex-wrap: wrap;
}
.cards{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 300px;

}
.cards svg{
    width: 50px;
    height: 50px;
    margin-bottom: 1rem;
    fill: rgb(78, 75, 75);
}
.cards p{
    margin-top: 1rem;
    text-align: justify;
    color: #929191;
}
</style>