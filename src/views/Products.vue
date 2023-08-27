<template>
  <div>
    <navbar-component></navbar-component>
    <main>
      <div
        class="relative pt-16 pb-32 flex content-center items-center justify-center"
        style="min-height: 75vh"
      >
        <div
          class="absolute top-0 w-full h-full bg-center bg-cover"
          style="
            background-image: url('https://github.com/nyah56/jjjj/blob/main/bg.jpg?raw=true');
          "
        >
          <span
            id="blackOverlay"
            class="w-full h-full absolute opacity-50 bg-black"
          ></span>
        </div>
        <div class="container z-10">
          <div class="items-center flex flex-wrap">
            <div class="w-full lg:w-6/12 px-4 ml-auto mr-auto text-center">
              <div class="flex justify-center">
                <div class="flex-col">
                  <img
                    src="../assets/img/logo.png"
                    alt=""
                    class="justify-center"
                  />
                  <h3 class="mt-4 text-lg text-red-400 font-semibold">
                    "Heavenly Bliss"
                  </h3>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="top-auto bottom-0 left-0 right-0 w-full absolute pointer-events-none overflow-hidden"
          style="height: 70px"
        >
          <svg
            class="absolute bottom-0 overflow-hidden"
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="none"
            version="1.1"
            viewBox="0 0 2560 100"
            x="0"
            y="0"
          >
            <polygon
              class="text-gray-300 fill-current"
              points="2560 0 2560 100 0 100"
            ></polygon>
          </svg>
        </div>
      </div>
      <section class="pb-20 bg-gray-300 -mt-24">
        <div class="container mx-auto lg:px-4 px-8">
          <div class="flex flex-wrap items-center mt-24">
            <h3
              class="text-3xl mb-4 font-semibold leading-normal mt-6 text-gray-700"
            >
              Produk Kami
            </h3>
            <div class="container lg:grid grid-cols-4 grid-rows-1 gap-4">
              <div :key="product.id" v-for="product in products">
                <Product :product="product" />
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
    <footer-component></footer-component>
  </div>
  <Widget
    phoneNumber="+6285945866020"
    companyName="Maviable"
    textReply="Tunggu Sebentar..."
    :messages="pesan"
  />
</template>

<script>
import NavbarComponent from '../components/Navbar.vue';
import FooterComponent from '../components/Footer.vue';
import Product from './Product.vue';
import Widget from '../components/Widget.vue';
import { products } from '../../data.js';
export default {
  name: 'products',

  data() {
    return {
      pesan: ['Hai,Apakah ada yang bisa dibantu?'],
      logo: '../assets/img/logo.png',
      products: products,
    };
  },
  components: {
    NavbarComponent,
    FooterComponent,
    Widget,
    Product,
  },
};
</script>
