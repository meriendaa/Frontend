<template>
	<div class="container d-flex justify-content-center align-items-center vh-100">
        <div class="card p-4 shadow-sm" style="max-width: 400px; width: 100%;">
        <h3 class="text-center mb-4">Login</h3>
            <div class="mb-3">
                <label for="user" class="form-label">User</label>
                <input v-model="mail" type="user" class="form-control" id="user" placeholder="Enter your user">
            </div>
            <div class="mb-3">
                <label for="password" class="form-label">Password</label>
                <input v-model="psw" type="password" class="form-control" id="password" placeholder="Enter your password">
            </div>
            <button @click="test" type="submit" class="btn btn-primary w-100">Login</button>
            <div class="mt-3 text-center">
                <router-link to="/forgotps">Forgot your password?</router-link>
            </div>
		
        </div>
    </div>

</template>
<script setup>
    import { ref } from 'vue';
    import { useRouter } from 'vue-router';

    const mail = ref();
    const psw = ref();
    function test()
    {
        console.log(mail.value);
        console.log(psw.value);
    }
    
</script>