<script lang="js" setup>
const props = defineProps(["drawer"]);
</script>

<template>
  <v-navigation-drawer v-model="props.drawer" location="left">
    <v-list>
      <v-list-item title="Navigation drawer"></v-list-item>

      <v-list-item>
        <NuxtLink to="/">Accueil</NuxtLink>
      </v-list-item>

      <v-list-item>
        <NuxtLink to="/login">Connexion</NuxtLink>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<style scoped></style>
