<template>
    <div class="profile_container">
        <div class="sidebar">
            <siderbar/>
        </div>
        <div class="mainArea">
            <orderPage/>
        </div>
    </div>
</template>
<script>
import orderPage from './order.vue';
import siderbar from './siderbar.vue';
// import orderPage
export default{
    name:"profilePage",
    components:{siderbar,orderPage}
}
</script>
<style scoped>
.profile_container{
    display: grid;
    grid-template-columns: 1fr 3fr;
}
.mainArea{
    display: flex;
    /* flex-direction: column; */
    justify-content: center;
    align-items: center;
}


</style>