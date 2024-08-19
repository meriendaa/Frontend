<template>
	<div class="container d-flex justify-content-center align-items-center vh-100">
        <div class="card p-4 shadow-sm" style="max-width: 400px; width: 100%;">
        <h3 class="text-center mb-4">Login</h3>
            <div class="mb-3">
                <label for="email" class="form-label">Email address</label>
                <input v-model="mail" type="email" class="form-control" id="email" placeholder="Enter your email">
            </div>
            <div class="mb-3">
                <label for="password" class="form-label">Password</label>
                <input v-model="psw" type="password" class="form-control" id="password" placeholder="Enter your password">
            </div>
            <button @click="test" type="submit" class="btn btn-primary w-100">Login</button>
            <div class="mt-3 text-center">
                <router-link to="/about">Forgot your password?</router-link>
            </div>
		
        </div>
    </div>

</template>
<script setup>
    import { ref } from 'vue';
    const mail = ref();
    const psw = ref();
    function test()
    {
        console.log(mail.value);
        console.log(psw.value);
    }
    
</script>