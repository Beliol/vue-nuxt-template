<script lang="js" setup>
const props = defineProps(["changeDrawer"]);
</script>

<template>
  <v-app-bar color="primary" prominent>
    <v-app-bar-nav-icon
      variant="text"
      @click="changeDrawer"
    ></v-app-bar-nav-icon>
    <v-toolbar-title>App bar</v-toolbar-title>
  </v-app-bar>
</template>

<style scoped></style>
