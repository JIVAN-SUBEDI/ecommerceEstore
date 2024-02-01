<template>
    <div class="container">

        <div class="footer_container">
            <div class="details">
                <h2>Estore.</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto, voluptatibus! Officiis molestias blanditiis ratione nemo quae nostrum dolorum autem facere.</p>
        </div>
        <div class="cards">
            <p>Quick links</p>
            <ul>
                <li><a href="#">About</a></li>
                <li><a href="#">Offers & Discounts</a></li>
                <li><a href="#">Get Coupoun</a></li>
                <li><a href="#">Contact Us</a></li>
            </ul>
        </div>
        <div class="cards">
            <p>Category</p>
            <ul>
                <li><a href="#">Women Cloth</a></li>
                <li><a href="#">Men Cloth</a></li>
                <li><a href="#">Winter Cloth</a></li>
                <li><a href="#">Summer Cloth</a></li>
            </ul>
        </div>
        <div class="cards">
            <p>Support</p>
            <ul>
                <li><a href="#">Frequently Asked Questions</a></li>
                <li><a href="#">Terms & Conditions</a></li>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Report a Payment Issue</a></li>
            </ul>
        </div>
    </div>
    <div class="copyright">
        Copyright &copy; 2024 Jivan Subedi. All Right Reserved
    </div>
</div>
</template>
<script>
export default{
    name:"footerVue"
}
</script>
<style scoped>
.container{
    padding: 2rem;
    height: calc(100vh - 80px);
    background: #f2f2f2;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}
.footer_container{
    display:grid;
    grid-template-columns: repeat(4,1fr);
    grid-gap: 1rem;
}
.cards ul li{
 list-style: none;
 margin-top: 0.5rem;
}
.copyright{
    color: #929191;
    height: 20%;
  
    display: flex;
    justify-content: center;
    align-items: center;
}
.details p{
    color: #929191;
    
}
a{
    color: #929191;
    text-decoration: none;
    transition: 0.5s ease-out;

}
a:hover{
    margin-left: 1rem;
    color: #1f79ff;
}
</style>