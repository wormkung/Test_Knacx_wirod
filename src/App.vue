<template>
  <Navbar />
  <div class="container mx-auto">
    <Carousel />
    <FlashSale />
    <Lazmall />
    <Catagory />
    <Product />
    <Footer />
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue";
import Carousel from "./components/carousel.vue";
import FlashSale from "./components/FlashSale.vue";
import Lazmall from "./components/Lazmall.vue";
import Catagory from "./components/Catagory.vue";
import Product from "./components/Product.vue";
import Footer from "./components/Footer.vue";
</script>

<style lang="scss" scoped></style>
