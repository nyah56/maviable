<template>
  <div id="app">
    <navbar-component></navbar-component>
    <Hero />
    <div>
      <main>
        <section class="pb-20 bg-gray-300 -mt-24">
          <router-view v-slot="{ Component, route }">
            <transition name="route" mode="out-in">
              <div :key="route.name">
                <component :is="Component"></component>
              </div>
            </transition>
          </router-view>
        </section>
      </main>
    </div>
    <footer-component></footer-component>
  </div>
</template>
<script>
import NavbarComponent from './components/Navbar.vue';
import FooterComponent from './components/Footer.vue';
import Hero from './views/Hero.vue';
export default {
  components: {
    NavbarComponent,
    FooterComponent,
    Hero,
  },
};
</script>
<style>
:root {
  --active: rgb(248 113 113);
}
a.router-link-exact-active {
  color: var(--active);
}
a.router-link-exact-active i {
  color: var(--active);
}
.route-enter-from {
  opacity: 0;
  transform: translateX(100px);
}
.route-enter-active {
  transition: all 0.3s ease-out;
}
.route-leave-to {
  opacity: 0;
  transform: translateX(-100px);
}
.route-leave-active {
  transition: all 0.3s ease-in;
}
@media only screen and (max-width: 640px) {
  .route-enter-from {
    opacity: 0;
    transform: translateY(100px);
  }
  .route-leave-to {
    opacity: 0;
    transform: translateY(-100px);
  }
}
</style>
