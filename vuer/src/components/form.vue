<template>
    <div>
<form name="login-form" @submit.prevent="login">
<label for="username">Enter Username</label>
<input type="text" v-model="user.username">
<label for="password">Enter Password</label>
<input type="password" v-model="user.password">
</form>
    </div>
</template>

<script setup>
import {reactive} from 'vue'
const user = reactive({username:'', password:''})
</script>

<style scoped>

</style>