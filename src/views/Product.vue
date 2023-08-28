<template>
  <div
    class="flex flex-col min-w-0 min-h-full lg:w-full w-5/6 break-words bg-white shadow-lg rounded-lg mb-8"
  >
    <img
      :src="imageSrc"
      alt="..."
      class="w-full align-middle rounded-t-lg h-full sm:h-48 object-cover"
    />
    <blockquote class="relative p-8 mb-4">
      <h4 class="text-xl font-bold text-gray-600">{{ product.name }}</h4>
      <p class="text-md font-light mt-2 text-gray-600 text-justify">
        {{ product.description }}
      </p>
    </blockquote>
  </div>
</template>

<script>
export default {
  name: 'Product',
  props: {
    product: Object,
  },

  computed: {
    imageSrc() {
      return new URL(`../assets/img/${this.product.src}.jpeg`, import.meta.url)
        .href;
    },
  },
};
</script>
