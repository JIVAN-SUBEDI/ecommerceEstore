<template>
    <div class="container">
        <div class="icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><path d="M80 0C44.7 0 16 28.7 16 64V448c0 35.3 28.7 64 64 64H304c35.3 0 64-28.7 64-64V64c0-35.3-28.7-64-64-64H80zm80 432h64c8.8 0 16 7.2 16 16s-7.2 16-16 16H160c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>
            <a>+977 98xxxxxxxx</a>
        </div>
        <div class="icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/></svg>
            <a>someone@example.com</a>
        </div>
    </div>
</template>
<script>
export default{
    name:"headerComp"
}
</script>
<style scoped>
.container{
    height: 30px;
    background: black;
    display:flex;
    align-items: center;
    justify-content: flex-end;
    padding: 0 1.5rem;
}
.icon{
    height: 100%;
    display: flex;
    align-items: center;
}
.icon svg{
    width: 20px;
    height: 20px;
    fill: #fff;
}
.icon a{
    font-size: 0.9rem;
    color: #fff;
    margin:0 0.5rem;
    font-weight: 200;
}
</style>