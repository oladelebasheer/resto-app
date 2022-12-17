<template>
  <img class="logo" alt="DeleSoft Tech logo" src="./assets/logo.png">
  <SignUp />

</template>

<script>
import SignUp from './components/SignUp.vue'
export default {
  name: 'App',
  components:{
    SignUp
  } 
}
</script>

<style>
@import './assets/css/style.css'
</style>
