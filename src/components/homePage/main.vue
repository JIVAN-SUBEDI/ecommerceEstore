<template>
    <headerComp/>
    <navbarVue/>
    <landingPageVue/>
    <categoryVue/>
    <latestProducts/>
    <newsletterVue/>
    <servicesVue/>
    <footerVue/>
</template>
<script>
import navbarVue from '../navbar.vue';
import footerVue from '../footer.vue';
import headerComp from '../header.vue';
import landingPageVue from './landingPage.vue';
import newsletterVue from './newsletter.vue';
import latestProducts from './latestProducts.vue';
import categoryVue from './category.vue';
import servicesVue from './services.vue';

export default{
    name:"homePage",
    components:{
        headerComp,
        navbarVue,
        servicesVue,
        landingPageVue,
        footerVue,
        newsletterVue,
        latestProducts,
        categoryVue
    }
}
</script>