<template>
  <hr class="h-14 bg-gray-200" />
  <div class="bg-gray-200">
    <p
      class="max-w-lg text-3xl font-semibold leading-normal text-gray-900 dark:text-white mx-3"
    >
      Lazmall
    </p>
    <div class="mx-3">
      <div>
        <div
          class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 justify-center items-center gap-4 mx-3"
        >
          <div
            v-for="(item, index) in product"
            :key="index"
            class="grid justify-center items-center bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
            style="height: 20rem"
          >
            <a href="#">
              <img
                width="150"
                class="p-8 rounded-t-lg"
                :src="item.image"
                alt="product image"
              />
            </a>
            <div class="px-5 pb-5">
              <a href="#">
                <h5
                  class="text-sm font-semibold tracking-tight text-gray-900 dark:text-white"
                >
                  {{ item.title }}
                </h5>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import axios from "axios";
import { ref, onMounted } from "vue";

const product = ref([]);

const fectdata = async () => {
  await axios
    .get("https://fakestoreapi.com/products?limit=6")
    .then((res) => {
      product.value = res.data;
      console.log(product.value);
    })
    .catch((err) => [console.log(err)]);
};

onMounted(() => fectdata());
</script>

<style lang="scss" scoped></style>
