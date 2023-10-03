<script lang="js" setup>
import AppBar from "~/features/AppBar.vue";
import NavBar from "~/features/NavBar.vue";

const drawer = ref(false);

function changeDrawer() {
  drawer.value = !drawer.value;
}
</script>

<template>
  <v-layout class="layout-app">
    <header>
      <AppBar :changeDrawer="changeDrawer" />
      <NavBar :drawer="drawer" />
    </header>

    <v-main class="main-app">
      <NuxtPage />
    </v-main>

    <v-footer class="footer-app" color="primary"></v-footer>
  </v-layout>
</template>

<style scoped>
.layout-app {
  display: flex;
  flex-direction: column;
}

.main-app {
  height: 90vh;
}

.footer-app {
  min-height: 10vh;
}
</style>