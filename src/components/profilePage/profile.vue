<template>
   
        <div class="form_container">
            <h3>Profile</h3>
            <div class="col">
                <label for="">Full Name</label>
                <input type="text" placeholder="Full Name">
            </div>
            <div class="col">
                <label for="">Phone No.</label>
                <input type="text" placeholder="Phone No.">
            </div>
            <div class="col">
                <label for="">Email</label>
                <input type="text" placeholder="Email">
            </div>
            <div class="col">
            <label for="">Gender</label>
            <br>
                <input type="radio" name="gender" ><span>Male</span>
                <input type="radio" name="gender" ><span>Female</span>
                <input type="radio" name="gender" ><span>Others</span>
            </div>
            <div class="col">
                <label for="">Date of birth</label>
                <input type="date" >
            </div>
            <div class="col">
                <label for="">Profile Picture</label>
                <input type="file" name="" id="">
            </div>
            <div class="buttonContainer">

                <button>Edit Profile</button>
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


input[type="text"], input[type="file"],input[type="date"]{
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
span{
    margin: 0 0.5rem;
}
</style>