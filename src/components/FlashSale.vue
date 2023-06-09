<template>
  <div class="bg-gray-200">
    <div class="flex justify-around mx-5 flex-wrap">
      <button
        type="button"
        class="md:text-2xl text-xs mt-5 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
      >
        Lazmall
      </button>
      <button
        type="button"
        class="md:text-2xl text-xs mt-5 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
      >
        คูปองลดเพิ่ม
      </button>
      <button
        type="button"
        class="md:text-2xl text-xs mt-5 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
      >
        เติมเงิน
      </button>
      <button
        type="button"
        class="md:text-2xl mt-5 text-xs text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
      >
        LazBlog
      </button>
      <button
        type="button"
        class="md:text-2xl text-xs mt-5 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
      >
        ร้านแนะนำ
      </button>
    </div>
    <hr class="h-6 bg-gray-200" />
    <p
      class="max-w-lg text-3xl font-semibold leading-normal text-gray-900 dark:text-white mx-3"
    >
      Flash Sale
    </p>

    <div class="mx-3 bg-white">
      <div class="flex justify-between">
        <div class="flex mt-3">
          <div>
            <h2 class="text-xs text-orange-500 mx-2 mt-1 md:text-base lg:mx-10">
              ลดราคาอยู่
            </h2>
          </div>
          <div>
            <h2 class="text-xs mx-3 md:text-base">
              สิ้นสุดใน
              <span
                ><button
                  type="button"
                  class="mx-2 focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sx px-2 py-1 mr-1 mb-3 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900"
                >
                  00
                </button>
                :
                <button
                  type="button"
                  class="focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sx px-2 py-1 mr-1 mb-1 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900"
                >
                  00
                </button></span
              >
            </h2>
          </div>
        </div>

        <div>
          <button
            type="button"
            class="mt-3 text-xs md:text-base text-orange-500 hover:text-white border border-orange-400 hover:bg-orange-500 focus:ring-4 focus:outline-none focus:ring-orange-300 font-medium rounded-lg md:mr-4 md:mb-4 text-center mr-2 mb-2 dark:border-orange-300 dark:text-orange-300 dark:hover:text-white dark:hover:bg-orange-400 dark:focus:ring-orange-900"
          >
            ช้อปสินค้าทั้งหมด
          </button>
        </div>
      </div>

      <hr class="mb-4 bg-black" />

      <div>
        <div
          class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 justify-center items-center gap-4 mx-3"
        >
          <div
            v-for="(item, index) in product"
            :key="index"
            class="grid justify-center items-center bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
            style="height: 22rem"
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
              <div class="flex items-center">
                <span class="text-sm font-bold text-orange-500 dark:text-white"
                  >฿{{ item.price }}</span
                >
              </div>
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

<style scoped></style>
