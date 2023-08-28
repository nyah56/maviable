<template>
  <div class="container mx-auto px-4">
    <div class="flex flex-wrap items-center mt-24">
      <h3
        class="text-3xl mb-2 font-semibold leading-normal mt-6 text-gray-700 lg:px-0 px-4"
      >
        About Us
      </h3>
    </div>
    <div class="flex flex-wrap mt-8">
      <div class="w-full lg:px-0 px-4">
        <p
          class="text-lg font-light leading-relaxed mt-4 mb-4 text-gray-700 text-justify"
        >
          Maviable Cheesecake, produk eksklusif kami, diolah dengan teliti dari
          bahan berkualitas tinggi sehingga menghadirkan pengalaman tak
          terlupakan bagi lidah Anda. Setiap gigitan membangkitkan kebahagiaan
          dengan kelezatan yang memanjakan, menciptakan harmoni sempurna dan
          cita rasa manis yang memukau, sesuai dengan motto kami "Heavenly
          Bliss". Cheesecake buatan kami menjadi puncak kenikmatan yang
          memanjakan indera dan menyentuh hati, menjadikan setiap momen istimewa
          dipenuhi dengan kebahagiaan tak tergantikan. Dengan Maviable
          Cheesecake, nikmati keindahan makanan penutup yang sesungguhnya.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import NavbarComponent from '../components/Navbar.vue';
import FooterComponent from '../components/Footer.vue';
// import Widget from '../components/Widget.vue';
export default {
  name: 'products',
  data() {
    return {
      pesan: ['Hai Pengunjung,Apakah yang bisa dibantu?'],
    };
  },
  components: {
    NavbarComponent,
    FooterComponent,
  },
};
</script>
