<template>
    <div class="container">
        <div class="login_container">
            <h2>Login</h2>
            <div class="flex">

                <div class="form_Container">
                    <div class="col">
                <label for="">Email<span class="text-danger">*</span></label>
                <input type="text" placeholder="someone@example.com">
            </div>
            <div class="col">
                <label for="">Password<span class="text-danger">*</span></label>
                <input type="password" placeholder="password">
            </div>
        </div>
        <div class="button_Container">
            <button class="login">Login</button>
            <p>OR</p>
            <button class="socialMedia facebook"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><path d="M80 299.3V512H196V299.3h86.5l18-97.8H196V166.9c0-51.7 20.3-71.5 72.7-71.5c16.3 0 29.4 .4 37 1.2V7.9C291.4 4 256.4 0 236.2 0C129.3 0 80 50.5 80 159.4v42.1H14v97.8H80z"/></svg> <span>Facebook</span></button>
            <button class="socialMedia google"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 488 512"><path d="M488 261.8C488 403.3 391.1 504 248 504 110.8 504 0 393.2 0 256S110.8 8 248 8c66.8 0 123 24.5 166.3 64.9l-67.5 64.9C258.5 52.6 94.3 116.6 94.3 256c0 86.5 69.1 156.6 153.7 156.6 98.2 0 135-70.4 140.8-106.9H248v-85.3h236.1c2.3 12.7 3.9 24.9 3.9 41.4z"/></svg> <span>Google</span></button>
        </div>
        </div>
    </div>
</div>
</template>
<script>
export default{
    name:"loginPage",
}
</script>
<style scoped>
.container{
    height: calc(100vh - 80px);
    display: flex;
    justify-content: center;
    align-items: center;
}
.login_container{
    width: 60%;
    padding: 1.5rem;
    background: #f2f2f2;
}
.flex{
    width:100%;
    
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 1.5rem;
}

.col{
    display: block;
    margin-bottom: 1rem;
}
.col input{
    width: 100%;
    height: 40px;
    border: 1px solid #929291;
    outline: none;
    padding: 0 1rem;
    border-radius: 5px;
}
h3{
    font-weight: 500;
    margin-bottom: 1.5rem;
}
.text-danger{
    color: red;
}
.login , .socialMedia{
    height: 40px;
    width: 100%;
    border-radius: 5px;
    cursor: pointer;
}
svg{
    width: 15px;
    height: 15px;
}
.button_Container p{
text-align: center;
color: #1f79ff;
margin-top:1rem;
}
.login{
    background: #1f79ff;
    border: 2px solid #1f79ff;
    color: white;
}
.facebook{
    background:  #316FF6;
    border: 2px solid #316FF6;
    
}
</style>