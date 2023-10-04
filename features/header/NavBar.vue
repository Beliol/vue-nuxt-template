<script lang="js" setup>
const props = defineProps(["drawer", "changeDrawer"]);
</script>

<template>
  <v-navigation-drawer v-model="props.drawer" location="left">
    <h3 class="text-center mb-5 mt-5">Navigation drawer</h3>
    <ul class="ma-2 listNav">
      <li class="pa-2">
        <NuxtLink class="linkButton" to="/" @click="changeDrawer"
          >Accueil
        </NuxtLink>
      </li>

      <li class="pa-2">
        <NuxtLink class="linkButton" to="/auth/login" @click="changeDrawer"
          >Connexion
        </NuxtLink>
      </li>
    </ul>
  </v-navigation-drawer>
</template>

<style scoped>
.listNav {
  text-align: center;
}

.linkButton {
  text-decoration: none;
  color: black;
}

li:hover {
  color: white;
  border: 1px solid black;
  border-radius: 5px;
}
</style>
