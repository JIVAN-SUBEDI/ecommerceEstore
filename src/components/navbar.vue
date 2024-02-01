<template>
    <div class="container">
        <div class="logo">Estore.</div>
        <!-- <ul class="menu">
            <li><a href="#">Home</a></li>
            <li><a href="#">Latest</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul> -->
        <div class="others">
            <div class="search">
                <input type="text" placeholder="Search Products..">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"/></svg>
            </div>
            <a class="icon">
                <div class="warning">05</div>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M225.8 468.2l-2.5-2.3L48.1 303.2C17.4 274.7 0 234.7 0 192.8v-3.3c0-70.4 50-130.8 119.2-144C158.6 37.9 198.9 47 231 69.6c9 6.4 17.4 13.8 25 22.3c4.2-4.8 8.7-9.2 13.5-13.3c3.7-3.2 7.5-6.2 11.5-9c0 0 0 0 0 0C313.1 47 353.4 37.9 392.8 45.4C462 58.6 512 119.1 512 189.5v3.3c0 41.9-17.4 81.9-48.1 110.4L288.7 465.9l-2.5 2.3c-8.2 7.6-19 11.9-30.2 11.9s-22-4.2-30.2-11.9zM239.1 145c-.4-.3-.7-.7-1-1.1l-17.8-20c0 0-.1-.1-.1-.1c0 0 0 0 0 0c-23.1-25.9-58-37.7-92-31.2C81.6 101.5 48 142.1 48 189.5v3.3c0 28.5 11.9 55.8 32.8 75.2L256 430.7 431.2 268c20.9-19.4 32.8-46.7 32.8-75.2v-3.3c0-47.3-33.6-88-80.1-96.9c-34-6.5-69 5.4-92 31.2c0 0 0 0-.1 .1s0 0-.1 .1l-17.8 20c-.3 .4-.7 .7-1 1.1c-4.5 4.5-10.6 7-16.9 7s-12.4-2.5-16.9-7z"/></svg>
            </a>
            <a class="icon">
                <div class="warning">05</div>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><path d="M0 24C0 10.7 10.7 0 24 0H69.5c22 0 41.5 12.8 50.6 32h411c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3H170.7l5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5H488c13.3 0 24 10.7 24 24s-10.7 24-24 24H199.7c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5H24C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"/></svg>
            </a>
            <a class="signIn button" >
                Sign In
            </a>
        </div>
    </div>
</template>
<script>
export default{
    name:"navbarComp"
}
</script>
<style scoped>
.container{
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding:0 1rem

}
.logo{
    font-size: 1.8rem;
    font-weight: 700;

}
.menu{
    display: flex;
}
.menu li{
    list-style: none;
    margin-right: 1.2rem;
}
.menu li a{
    color:black;
    text-decoration: none;
    font-weight: 0.9rem;
}
.menu li a:hover{
   color: red;
}
.others{
    display: flex;
    align-items: center;
}
.search{
    position: relative;
    display: flex;
    align-items: center;
    margin-right: 1rem;
}
.search input{
    width: 250px;
    height: 40px;
    border-radius: 22.5px;
    outline: none;
    border: 1px solid #929191;
    padding: 1rem 1.8rem 1rem 1rem;
}
.search svg{
    position: absolute;
    fill: #929191;
    width: 15px;
    height: 15px;
    right: 0.8rem;
}
.icon{
    height: 40px;
    width: 40px;
    border-radius: 50%;
    border: 1px solid #929191;
    background: transparent;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 1rem;
}
.icon svg{
    width: 20px;
    height: 20px;
    fill: #1f1e1e;

}
.icon .warning{
    background: #09acff;
    color: white;
    font-size: 0.7rem;
    padding: 4px;
    border-radius: 50%;
    position: absolute;
    right: -8px;
    top: -10px;
}
.signIn{
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding:0.5rem 1rem;
    background: #1f79ff;
    border: 2px solid #1f79ff;
    color: white;
    border-radius: 10px;
}


</style>