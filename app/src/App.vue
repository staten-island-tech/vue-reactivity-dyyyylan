<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="" class="logo" src="@/assets/logo.png" width="150" height="150" />

    <div class="wrapper">
      <nav>
        <RouterLink class="thething px-6 py-2 bg-gray-400 text-white rounded-lg shadow-lg hover:bg-gray-600 hover:shadow-xl transition duration-200 ease-in-out" to="/">Shop</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>


@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
