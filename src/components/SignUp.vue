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
                <span class="input-group-text">
                    <font-awesome-icon icon="fa-solid fa-user" />
                </span>
              <input icon="fa-solid fa-user-secret" type="email" class="form-control my-3" placeholder="Enter name">
            </div>
            <div class="mb-3">
                <span class="input-group-text">
                    <font-awesome-icon icon="fa-solid fa-user-secret" />
                </span>
                <input type="email" class="form-control" placeholder="Email address">
              </div>
            <div class="mb-3">
                <span class="input-group-text">
                    <font-awesome-icon icon="fa-solid fa-user-secret" />
                </span>
              <input type="password" class="form-control" placeholder="Enter password">
            </div>
            <div class="d-grid gap-2">
            <button type="submit" class="btn btn-primary lg">Sign Up</button></div>
            <div class="mb-4 mt-3">
            <a href="#">Forgot password</a>
        </div>
            <div class="mb-3">
                <p>Don't have an account <a href="#">Sign Up here</a></p>
            </div>
          </form>
        </div>
        </div>
    </div>
</section>
</template>

<script>
export default{
    name:'SignUp'
}
</script>