<template>
    <div class="container">
        <headerVue/>
        <navbarVue/>
        <div class="mainContainer">
            <formVue/>
            <productVue/>
        </div>
        <footerVue/>
    </div>
</template>
<script>
import footerVue from '../footer.vue'
import navbarVue from '../navbar.vue'
import headerVue from '../header.vue';
import formVue from './form.vue';
import productVue from './product.vue';

export default{
    name:"contactPage",
    components:{
        footerVue,
        navbarVue,
        headerVue,
        formVue,
        productVue
    }
}
</script>
<style scoped>
.mainContainer{
    width: 100%;
    padding: 2rem;
    display: grid;
    grid-template-columns: 1fr 3fr;
    grid-gap: 1rem;
    
}
</style>