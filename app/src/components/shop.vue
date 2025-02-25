<template>
  <div class="flex">

    <div class="flex flex-col w-[20vw] min-h-screen bg-gray-200 p-4 shadow-lg">
      <div v-for="shop in shops" :key="shop.name"
           class="card w-full mb-4 p-4 bg-white shadow-md rounded-lg text-center">
        <h3 class="text-lg font-bold">{{ shop.name }}</h3>
        <img :src="shop.image" :alt="shop.image" class="w-full h-auto rounded-md">
        <h2 class="text-sm mt-2">{{ "Price: $" + shop.price }}</h2>
        <button type="submit" class="addtocart px-6 py-2 bg-gray-400 text-white rounded-lg shadow-lg hover:bg-gray-600 hover:shadow-xl transition duration-200 ease-in-out" @click="addToCart(shop)">Add to cart</button>
      </div>
    </div>

    <div class="relative w-[40%] left-[14vw]">

          <h2 class="text-lg font-bold">Cart Items:</h2>
          <ul>
            <li v-for="(item) in cart" :key="item.name" class="mt-2">
              {{ item.name }} - ${{ item.price }}
              <button @click="removeFromCart(item)" class="ml-2 px-2 py-1 bg-red-500 text-white rounded">X</button>
            </li>
          </ul>
 

    </div>
  </div>
</template>

<script setup>
import { ref, defineProps } from 'vue';


defineProps({
  shop: Object
});

const cart = ref([]);


const addToCart = (shop) => {
  cart.value.push(shop);

};

const removeFromCart = (itemToRemove) => {
  const index = cart.value.findIndex(item => item.name === itemToRemove.name);
  if (index !== -1) {
    cart.value.splice(index, 1);
  }
};
const shops = [
  { name: "banana", price: 4999.99, image: "banana.jpg" },
  { name: "broccoli", price: 1.49, image: "broc.jpg" },
  { name: "carrot", price: 5.79, image: "carrot.jpg" },
  { name: "potato", price: 60.19, image: "potato.jpg" },
  { name: "tomato", price: 4.20, image: "tomato.jpg" },
  { name: "milk", price: 10000.00, image: "milk.jpg" },
  { name: "eggs", price: 300.00, image: "eggs.jpg" },
  { name: "Tyler Tyndale", price: 0.50, image: "tyler.jpg"},
  { name: "avocado", price: 3, image: "image.png"}
];


</script>

<style scoped>

</style>

