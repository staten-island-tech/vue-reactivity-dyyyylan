<template>
    <div>
<div v-for="item in items" :key="item.id">
    {{ item }}
</div>
    </div>
</template>

<script setup>
import { reactive } from "vue";

const store = reactive[
    cart = []
]

</script>

<style scoped>

</style>