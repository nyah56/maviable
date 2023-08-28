<template>
 <div class="container mx-auto px-4">
          <div class="flex flex-wrap">
            <div class="lg:pt-12 pt-6 w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg z-20"
              >
                <div class="px-4 py-5 flex-auto ">
                  <div
                    class="text-white p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-green-400"
                  >
                    <i class="fas fa-dollar-sign"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Terjangkau</h6>
                  <p class="mt-2 mb-4 text-gray-600">Nikmati Dessert tanpa menguras kantong</p>
                </div>
              </div>
            </div>
            <div class="w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg z-20"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="text-white p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-red-400"
                  >
                    <i class="fas fa-heart"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Sehat</h6>
                  <p class="mt-2 mb-4 text-gray-600">
                    Dibuat dengan bahan alami dan kualitasnya selalu dijaga
                  </p>
                </div>
              </div>
            </div>
            <div class="pt-6 w-full md:w-4/12 px-4 text-center">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-8 shadow-lg rounded-lg z-20"
              >
                <div class="px-4 py-5 flex-auto">
                  <div
                    class="text-white p-3 text-center inline-flex items-center justify-center w-12 h-12 mb-5 shadow-lg rounded-full bg-pink-400"
                  >
                    <i class="fas fa-jar"></i>
                  </div>
                  <h6 class="text-xl font-semibold">Variatif</h6>
                  <p class="mt-2 mb-4 text-gray-600">
                    Pilih Topping pada setiap cupnya sesuai keinginanmu
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="flex flex-wrap items-center mt-24">
            <div class="w-full md:w-5/12 px-4 mr-auto ml-auto">
              <div
                class="text-gray-600 p-3 text-center inline-flex items-center justify-center w-16 h-16 mb-6 shadow-lg rounded-full bg-gray-100"
              >
                <i class="fas fa-jar text-xl"></i>
              </div>
              <h3
                class="text-3xl mb-2 font-semibold leading-normal text-gray-700"
              >
                Maviable
              </h3>
              <p
                class="text-lg font-light leading-relaxed mt-4 mb-4 text-gray-700 text-justify"
              >
                Kami menyediakan Cheesecake yang terbuat dari bahan berkualitas
                tinggi dan Untuk pengiriman daerah Malang Sawojajar dan
                Sekitarnya Free Ongkir.
              </p>

              <router-link
                :to="{ name: 'products' }"
                class="text-lg font-light leading-relaxed mt-4 mb-4 text-gray-700"
                >Lihat Produk...</router-link
              >
            </div>
            <div class="w-full md:w-4/12 px-4 mr-auto ml-auto">
              <div
                class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded-lg"
              >
                <img
                  alt="..."
                  src="../assets/img/hero.jpeg"
                  class="w-full align-middle rounded-t-lg h-full sm:h-48 object-cover"
                />
                <blockquote class="relative p-8 mb-4">
                  <svg
                    preserveAspectRatio="none"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 583 95"
                    class="absolute left-0 w-full block"
                    style="height: 95px; top: -94px"
                  >
                   
                  </svg>
                  <h4 class="text-xl font-bold text-gray-600">Cheesecake</h4>
                  <p class="text-md font-light mt-2 text-gray-600">
                    Kami Menyediakan Cheesecake dengan 4 jenis rasa :
                    <ul class="mt-4">
                      <li class="text-md font-light mt-2 text-gray-600">Strawberry</li>
                      <li class="text-md font-light mt-2 text-gray-600">Blueberry</li>
                      <li class="text-md font-light mt-2 text-gray-600">Red Velvet</li>
                      <li class="text-md font-light mt-2 text-gray-600">Chocolate</li>
                    </ul>
                  </p>
                  <p class="text-md font-light mt-4 text-gray-600">
                    Dengan Ukuran <span class="font-bold">Medium</span> dan <span class="font-bold">Large</span>
                  </p>
                </blockquote>
              </div>
            </div>
          </div>
        </div>
</template>
<script>


export default {
  name: 'home',
};
</script>
