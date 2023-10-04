<script lang="js" setup>
import AuthApp from "~/features/auth/AuthApp.vue";

const route = useRoute();

const features = {
  login: AuthApp,
};

const activeFeature = computed(() => features[route.params.mode] ?? null);
</script>

<template>
  <component :is="activeFeature"></component>
</template>