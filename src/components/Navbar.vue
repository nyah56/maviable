<template>
  <nav
    class="top-0 absolute z-50 w-full flex flex-wrap items-center justify-between px-2 py-3"
  >
    <div
      class="container px-4 mx-auto flex flex-wrap items-center justify-between"
    >
      <div
        class="w-full relative flex justify-between lg:w-auto lg:static lg:block lg:justify-start"
      >
        <button
          class="cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
          type="button"
          @click="toggleNavbar"
        >
          <i class="text-white fas fa-bars"></i>
        </button>
      </div>
      <div
        class="lg:flex flex-grow items-center bg-white lg:bg-transparent lg:shadow-none"
        :class="{ hidden: !showMenu, block: showMenu }"
      >
        <ul class="flex flex-col lg:flex-row list-none mr-auto">
          <li class="flex items-center">
            <router-link
              :to="{ name: 'home' }"
              class="lg:text-white lg:hover:text-red-500 text-gray-800 px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold"
              @mouseover="isHover = true"
              @mouseout="isHover = false"
            >
              <i
                :class="isHover ? 'lg:hover:text-red-500' + homeIcon : homeIcon"
              ></i>
              Home
            </router-link>
          </li>
          <li class="flex items-center">
            <router-link
              :to="{ name: 'products' }"
              class="lg:text-white lg:hover:text-red-500 text-gray-800 px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold"
              @mouseover="isHover = true"
              @mouseout="isHover = false"
            >
              <i
                :class="
                  isHover
                    ? 'lg:hover:text-red-500' + productsIcon
                    : productsIcon
                "
              ></i>
              Products
            </router-link>
          </li>
          <li class="flex items-center">
            <router-link
              :to="{ name: 'about' }"
              class="lg:text-white lg:hover:text-red-500 text-gray-800 px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold"
              @mouseover="isHover = true"
              @mouseout="isHover = false"
            >
              <i
                :class="
                  isHover ? 'lg:hover:text-red-500' + aboutIcon : aboutIcon
                "
              ></i>
              About Us
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isHover: false,
      showMenu: false,
      homeIcon: 'lg:text-gray-300  fa-solid fa-home text-lg leading-lg mr-2',
      productsIcon: 'lg:text-gray-300 fa-solid fa-jar text-lg leading-lg mr-2',
      aboutIcon: 'lg:text-gray-300 far fa-building text-lg leading-lg mr-2',
    };
  },
  methods: {
    toggleNavbar() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>
