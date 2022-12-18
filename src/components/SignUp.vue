<template>
<section class="form my-4 mx-5 signup">
    <div class="container">
        <div class="row g-0">
            <div class="col-lg-6">
                <img class="img-fluid" src="../../public/reg.jpg" alt="alternative signup image" />
            </div>
            <div class="col-lg-6 px-5 pt-5">
                <img class="logo" alt="DeleSoft Tech logo" src="../assets/logo.png" /><hr>
                <h1 class="fw-bold text-capitalize py-2">Sign Up</h1>
                
                <form>
                    <div class="mb-3">
                        <input type="text" class="form-control my-3" placeholder="Enter name" v-model="name">
                    </div>

                    <div class="mb-3">
                        <input type="email" class="form-control" placeholder="Email address" v-model="email">
                    </div>

                    <div class="mb-3">
                        <input type="password" class="form-control" placeholder="Enter password" v-model="password">
                    </div>

                    <div class="d-grid gap-2 mb-3">
                        <button type="submit" class="btn btn-primary lg" v-on:click="signUp()">Sign Up</button>
                    </div>

                </form>
            </div>
        </div>
    </div>
</section>
</template>

<script>
import axios from 'axios'

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
            let result = await axios.post("http://localhost:3000/users", {
                email: this.email,
                name:this.name,
                password:this.password
            });
            console.warn("result");
            if(result.status==201){
                localStorage.setItem("user-info", JSON.stringify(result.data))
                this.$router.push({name:'Home'})
            }
        }
    }
}
</script>
