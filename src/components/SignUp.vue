<template>
    <section class="form my-4 mx-5 signup">
    <div class="container">
        <div class="row g-0">
            <div class="col-lg-6">
                <img class="img-fluid" src="../../public/reg.jpg" alt="alternative signup image" srcset="">
                </div>
            <div class="col-lg-6 px-5 pt-5">
                <h1 class="fw-bold text-capitalize py-3">Sign Up</h1>
        <form>
            <div class="mb-4 input-group">
              <input icon="fa-solid fa-user-secret" 
              type="email" class="form-control my-3" 
              placeholder="Enter name" v-model="name">
            </div>
            <div class="mb-3">
                <input type="email" class="form-control" placeholder="Email address" v-model="email">
              </div>
            <div class="mb-3">
              <input type="password" class="form-control" placeholder="Enter password" v-model="password">
            </div>
            <div class="d-grid gap-2">
            <button type="submit" class="btn btn-primary lg" v-on:click="signUp()">Sign Up</button></div>
          </form>
        </div>
        </div>
    </div>
</section>
</template>

<script>
export default{
    name:'SignUp',
    data(){
        return{
            name:'',
            email:'',
            password:''
        }
    },
    methods:{
        signUp(){
            console.warn("Signed up", this.name, this.email, this.password)
        }
    }
}
</script>