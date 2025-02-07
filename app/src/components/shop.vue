<template>
    <div class="container flex m-auto px-[5vw] flex-wrap justify-around w-[85vw] rounded">
<div v-for="shop in shops" :key="shop.name" class="">
</div>
    </div>
</template>

<script setup>

const shop = [
  { name: "banana", price: 0.5, image: "banana.jpg" },
  { name: "broccoli", price: 1.2, image: "broccoli.jpg" },
  { name: "carrot", price: 0.8, image: "carrot.jpg" },
  { name: "potato", price: 0.6, image: "potato.jpg" },
  { name: "tomato", price: 1.0, image: "tomato.jpg" },
  { name: "milk", price: 2.5, image: "milk.jpg" },
  { name: "eggs", price: 3.0, image: "eggs.jpg" },
  { name: "Tyler Tyndale", price: 5.0, image: "tyler.jpg"}
];

</script>

<style scoped>

</style>
