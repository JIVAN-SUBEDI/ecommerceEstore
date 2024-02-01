<template>
    <div class="sidebar_container">
        <h3>Manage Your Account</h3>
        <ul>
            <li><a href="">Profile</a></li>
            <li><a href="">orders</a></li>
            <li><a href="">Reviews</a></li>
            <li><a href="">Logout</a></li>
        </ul>
    </div>
</template>
<script>
export default{
    name:"sideBar"
}
</script>
<style scoped>
.sidebar_container{
    background: #f2f2f2;
    height: 100vh;
}
.sidebar_container li{
list-style: none;
width: 100%;
padding: 1rem;
display: flex;
justify-content: center;
align-items: center;
border-bottom: 1px solid #929291;
}
.sidebar_container li a{
    color: black;
    text-decoration: none;
    transition: 0.3s ease-in-out;
}
.sidebar_container li a:hover{
    color: #1f79ff;
    margin-left:3rem ;
}
h3{
    font-weight: 500;
    padding: 1rem;
}
</style>