<!-- eslint-disable vue/multi-word-component-names -->
<template>
<div class="container">
    <h1>Welcome to Home page</h1>
</div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Home',
    mounted() {
        let user = localStorage.getItem('user-info')
        if (!user) {
            this.$router.push({ name: 'SignUp' })
        }
    }
}
</script>
