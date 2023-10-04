<script lang="js" setup>
//Variables
const login = ref("");
const password = ref("");

const rulesForm = {
  required: (value) => !!value || "Champ obligatoire",
};

//Hook
const router = useRouter();
</script>

<template>
  <div class="form-div">
    <v-sheet class="form-login" width="300">
      <h2 class="mb-5">Login</h2>
      <v-form fast-fail @submit.prevent>
        <v-text-field
          v-model="login"
          :rules="[rulesForm.required]"
          label="Login"
        ></v-text-field>

        <v-text-field
          v-model="password"
          :rules="[rulesForm.required]"
          label="Password"
          type="password"
        ></v-text-field>

        <v-btn class="mt-2" type="submit">Submit</v-btn>
        <v-btn class="mt-2 ml-2" @click="router.push('/register')"
          >Register
        </v-btn>
      </v-form>
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