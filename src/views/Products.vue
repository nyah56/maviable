<template>
  <div class="container mx-auto lg:px-4 px-8">
    <div class="flex flex-wrap items-center mt-24">
      <h3 class="text-3xl mb-4 font-semibold leading-normal mt-6 text-gray-700">
        Produk Kami
      </h3>
      <div class="container lg:grid grid-cols-4 grid-rows-1 gap-4">
        <div :key="product.id" v-for="product in products">
          <Product :product="product" />
        </div>
      </div>
    </div>
  </div>
  <Widget
    phoneNumber="+6285945866020"
    companyName="Maviable"
    textReply="Tunggu Sebentar..."
    :messages="pesan"
  />
</template>

<script>
import Product from './Product.vue';
import Widget from '../components/Widget.vue';
import { products } from '../../data.js';
export default {
  name: 'products',

  data() {
    return {
      pesan: ['Hai,Apakah ada yang bisa dibantu?'],
      products: products,
    };
  },

  components: {
    Widget,
    Product,
  },
};
</script>
