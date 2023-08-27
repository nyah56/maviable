<template>
  <footer class="relative bg-gray-800 pt-8 pb-6 lg:px-4 px-8">
    <div
      class="bottom-auto top-0 left-0 right-0 w-full absolute pointer-events-none overflow-hidden -mt-20"
      style="height: 80px"
    >
      <svg
        class="absolute bottom-0 overflow-hidden"
        xmlns="http://www.w3.org/2000/svg"
        preserveAspectRatio="none"
        version="1.1"
        viewBox="0 0 2560 100"
        x="0"
        y="0"
      ></svg>
    </div>
    <div class="container mx-auto px-auto flex justify-between">
      <div class="w-full">
        <div class="container flex lg:flex-row flex-col">
          <div class="lg:w-1/2 mb-8">
            <h4 class="text-3xl font-semibold text-white">Hubungi Kami</h4>
            <h5 class="text-lg mb-2 text-gray-300 mt-4">
              Pada Sosial Media berikut.
            </h5>
            <div class="mt-6">
              <a
                class="bg-white lg:hover:bg-gray-300 shadow-lg font-normal h-10 w-10 items-center justify-center align-center rounded-full outline-none focus:outline-none mr-2 p-3"
                href="https://wa.me/6285945866020"
                target="_blank"
                ><i
                  class="lg:text-green-400 text-green-400 fab fa-whatsapp text-lg leading-lg"
                ></i
                ><span class="lg:hidden inline-block ml-2 text-gray-600"
                  >Whatsapp</span
                ></a
              >
              <a
                class="bg-white lg:hover:bg-gray-300 shadow-lg font-normal h-10 w-10 items-center justify-center align-center rounded-full outline-none focus:outline-none mr-2 p-3"
                href="https://instagram.com/maviable.mlg"
                target="_blank"
                ><i
                  class="lg:text-pink-400 text-pink-400 fab fa-instagram text-lg leading-lg"
                ></i
                ><span class="lg:hidden inline-block ml-2 text-gray-600"
                  >Instagram</span
                ></a
              >
            </div>
          </div>
          <div class="w-1/2 lg:text-right text-white">
            <span class="block uppercase text-sm font-semibold mb-4"
              >Halaman</span
            >
            <ul class="list-unstyled">
              <li>
                <router-link :to="{ name: 'home' }">Home</router-link>
              </li>
              <li>
                <router-link :to="{ name: 'products' }">Products</router-link>
              </li>
              <li>
                <router-link :to="{ name: 'about' }">About</router-link>
              </li>
            </ul>
          </div>
        </div>

        <hr class="my-8 border-gray-400" />
        <div class="w-full md:w-4/12 px-4 mx-auto text-center">
          <div class="text-sm text-gray-200 font-semibold py-1">
            Copyright © {{ date }} Maviable
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  data() {
    return {
      date: new Date().getFullYear(),
    };
  },
};
</script>
