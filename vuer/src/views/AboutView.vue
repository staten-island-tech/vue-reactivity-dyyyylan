<template>
  <div>
    <form name="login-form" @submit.prevent="login">
<label for="username">Enter Username</label>
<input type="text" v-model="user.username">
<label for="password">Enter Password</label>
<input type="password" v-model="user.password">
<button type="submit">sign in</button>
</form>
<h2 v-if="skibidi">Mark Fridlin</h2>
<h2 v-else>ryan chen</h2>
  </div>
</template>

<script setup>
import {reactive} from 'vue'
const user = reactive({username:'', password:''})
const skibidi = false
</script>

<style scoped>

</style>