<template>
  <div class="container">
    <nav class="bg-gray-100 dark:bg-gray-700">
      <div class=" ">
        <div class="flex items-center justify-end">
          <ul class="flex flex-wrap mt-0 space-x-6 text-sm">
            <li>
              <a
                href="#"
                class="text-gray-900 dark:text-white hover:text-orange-500"
                >item1</a
              >
            </li>
            <li>
              <a
                href="#"
                class="text-gray-900 dark:text-white hover:text-orange-500"
                >item2
              </a>
            </li>
            <li>
              <a
                href="#"
                class="text-gray-400 dark:text-white hover:text-orange-500"
                >item3</a
              >
            </li>
            <li>
              <a
                href="#"
                class="text-gray-400 dark:text-white hover:text-orange-500"
                >item4</a
              >
            </li>
            <li>
              <a
                href="#"
                class="text-gray-400 dark:text-white hover:text-orange-500"
                >item5</a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- navbar -->
    <div class="flex mt-0">
      <div class="flex-grow h-20">
        <nav
          class="bg-white dark:bg-gray-900 fixed w-full border-b border-gray-200 dark:border-gray-600"
        >
          <div
            class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4"
          >
            <a href="#" class="flex items-center">
              <img
                src="https://laz-img-cdn.alicdn.com/images/ims-web/TB1KB2laMFY.1VjSZFnXXcFHXXa.png"
                class="h-8 md:h-10"
                alt="Flowbite Logo"
              />
            </a>

            <div class="flex md:order-2">
              <a href="#" class="flex items-center">
                <img
                  src="https://laz-img-cdn.alicdn.com/images/ims-web/TB1DcZESBr0gK0jSZFnXXbRRXXa.jpg"
                  class="h-8 md:h-10"
                  alt="Flowbite Logo"
                />
              </a>
              <button
                data-collapse-toggle="navbar-sticky"
                type="button"
                class="inline-flex items-center p-2 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
                aria-controls="navbar-sticky"
                aria-expanded="false"
              >
                <span class="sr-only">Open main menu</span>
                <svg
                  class="w-6 h-6"
                  aria-hidden="true"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                    clip-rule="evenodd"
                  ></path>
                </svg>
              </button>
            </div>

            <div
              class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1"
              id="navbar-sticky"
            >
              <!-- input -->
              <form class="flex items-center content-center">
                <div class="relative w-full">
                  <div
                    class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
                  >
                    <svg
                      aria-hidden="true"
                      class="w-6 h-6 text-gray-500 dark:text-gray-400"
                      fill="currentColor"
                      viewBox="0 0 20 20"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        fill-rule="evenodd"
                        d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                        clip-rule="evenodd"
                      ></path>
                    </svg>
                  </div>
                  <input
                    type="text"
                    id="simple-search"
                    class="bg-gray-100 h-12 text-gray-900 text-sm block w-full pl-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                    placeholder="ค้นหาในลาซาด้า"
                    required
                  />
                </div>
                <button
                  type="submit"
                  class="h-12 p-2.5 text-sm font-medium text-white bg-orange-700 hover:bg-orange-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                >
                  <svg
                    class="w-5 h-5"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                    ></path>
                  </svg>
                </button>
                <svg
                  aria-hidden="true"
                  class="w-12 h-12 md:ml-10"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M3 1a1 1 0 000 2h1.22l.305 1.222a.997.997 0 00.01.042l1.358 5.43-.893.892C3.74 11.846 4.632 14 6.414 14H15a1 1 0 000-2H6.414l1-1H14a1 1 0 00.894-.553l3-6A1 1 0 0017 3H6.28l-.31-1.243A1 1 0 005 1H3zM16 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM6.5 18a1.5 1.5 0 100-3 1.5 1.5 0 000 3z"
                  ></path>
                </svg>
              </form>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from "vue";
import { initCarousels, initDropdowns } from "flowbite";

onMounted(() => {
  initCarousels();
  initDropdowns();
});
</script>

<style lang="scss" scoped></style>
