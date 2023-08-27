<template>
  <div id="app">
    <router-view />
  </div>
</template>
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
</style>
