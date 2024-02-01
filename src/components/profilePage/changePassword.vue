<template>
    <template>
   
   <div class="form_container">
       <h3>Change Password</h3>
       <div class="col">
           <label for="">Old Password</label>
           <input type="text" placeholder="Old Password">
       </div>
       <div class="col">
           <label for="">New Password</label>
           <input type="text" placeholder="New Password">
       </div>

       <div class="buttonContainer">

           <button>Change Password</button>
       </div>
 
</div>
</template>
<script>
export default{
name:"profileVue"
}
</script>
<style scoped>
.form_container{
background: #f2f2f2;
border-radius: 5px;
width: 80%;
padding: 1.5rem;
}
label{
font-size: 0.8rem;
}


input[type="text"]{
width: 100%;
height: 45px;
border: 1px solid #929291;
outline: none;
border-radius: 5px;
padding: 0 1rem;
}
h3{
font-weight: 500;
}
button{
height: 45px;
background:#1f79ff;
width: 40%;
margin-top: 2rem;
border: 2px solid #1f79ff;
color: white;
border-radius: 5px;
}
button:hover{
background: transparent;
color: #1f79ff;
cursor: pointer;
}
.buttonContainer{
width: 100%;
display: flex;
justify-content: space-around;
}

</style>
</template>