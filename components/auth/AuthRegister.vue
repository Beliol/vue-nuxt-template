<script lang="js" setup>
const props = defineProps(["fields", "rulesForm"]);

//Hook
const router = useRouter();
</script>

<template>
  <div class="form-div">
    <v-sheet class="form-login" width="300">
      <h2 class="mb-5">Login</h2>
      <v-form v-for="field in fields" fast-fail @submit.prevent>
        <v-text-field
          v-model="field.name"
          :rules="[rulesForm]"
          class="ma-1"
          label="{{field.label}}"
          type="{{field.type}}"
        ></v-text-field>
      </v-form>
      <v-btn class="mt-2">Login</v-btn>
      <v-btn class="mt-2 ml-2" @click="router.push('/register')"
        >Register
      </v-btn>
    </v-sheet>
  </div>
</template>

<style scoped>
.form-div {
  display: flex;
  justify-content: center;
}

.form-login {
  display: flex;
  flex-direction: column;
  text-align: center;
  margin-top: 5%;
  width: 100vw;
}
</style>
