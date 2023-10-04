<script lang="js" setup>
import AuthLogin from "~/components/auth/AuthLogin.vue";

const fields = [
  { name: "username", label: "Username", type: "text", isRequired: true },
  { name: "password", label: "Password", type: "password", isRequired: true },
];
</script>

<template>
  <AuthLogin :fields="fields" />
</template>