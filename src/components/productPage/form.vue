<template>
    <div class="container">
        <h3>Filter Product</h3>
        <div class="search">
            <input type="search" name="" id="" placeholder="Search Product...">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"/></svg>
        </div>
        <div class="select">
            <h4>Category</h4>
            <select name="" id="">
                <option value="">Category1</option>
                <option value="">Category2</option>
                <option value="">Category3</option>
                <option value="">Category4</option>
            </select>
        </div>
        <div class="select">
            <h4>Brand</h4>
            <select name="" id="">
                <option value="">brand1</option>
                <option value="">brand2</option>
                <option value="">brand3</option>
                <option value="">brand4</option>
            </select>
        </div>
    </div>
</template>
<script>
export default{
    name:"formVue"
}
</script>
<style scoped>
.container{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.search{
    width:100%;
    display: flex;
    align-items: center;
    position:relative;
}
.search input{
    width:100%;
    height:45px;
    border-radius: 22.5px;
    background: #eee;
    border:1px solid #929191;
    padding:0 1rem;
    outline: none;

}
.search svg{
    position: absolute;
    width: 15px;
    height: 15px;
    fill: #929191;
    right: 10px;
}
h3{
    align-self: flex-start;
    font-weight: 400;
    margin-bottom: 1rem;
}
.select{
    margin-top: 1.5rem;
    width:100%;

}
.select select{
    width:100%;
    height:45px;
    border-radius: 22.5px;
    background: #eee;
    border:1px solid #929191;
    padding:0 1rem;
    outline: none;
    margin-top: 0.5rem;
}
h4{
    font-weight: 400;
}
</style>