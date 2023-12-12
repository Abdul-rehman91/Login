<template>
    <div class="registartion-from">
        <div class="mb-3">
            <label for="exampleInputName" class="form-label">Name</label>
            <input v-model="name" type="text" class="form-control" id="exampleInputName">

        </div>
        <div class="mb-3">
            <label for="exampleInputEmail1" class="form-label">Email address</label>
            <input v-model="email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">

        </div>
        <div class="mb-3">
            <label for="exampleInputPassword1" class="form-label">Password</label>
            <input v-model="password" type="password" class="form-control" id="exampleInputPassword1">
        </div>

        <button v-on:click="signUp" class="btn btn-primary">Submit</button>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    
    name: 'SignUp',

    data() {
        return {
            name: '',
            email: '',
            password: ''
        }
    },
    methods: {
       async signUp() {
            console.warn("SignUp Clicked", this.name, this, this.password, this.email)
        let result = await axios.post("http://localhost:3000/user",{
            email:this.email,
            name:this.name,
            password:this.password,
        });
        console.warn(result);
        if(result.status==201){
            alert("Working")
        }
        localStorage.setItem("user-info", JSON.stringify(result.data))
        }
    }
}

</script>
<style>
.registartion-from {
    width: 40%;
    margin: 10px auto;
    border: 2px solid black;
    padding: 20px 10px;
    border-radius: 5px;
}

.btn {
    color: #fff;
    background-color: black;
    border: 2px solid white;
}

.btn:hover {
    background-color: #fff;
    color: #000;
    border: 2px solid black;
}
</style>