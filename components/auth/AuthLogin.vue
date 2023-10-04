<script lang="js" setup>
const props = defineProps(["fields"]);
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
        <div v-for="field in props.fields">
          <v-text-field
            v-model="field.name"
            :label="field.label"
            :rules="[field.isRequired && rulesForm.required]"
            :type="field.type"
            class="ma-1"
          ></v-text-field>
        </div>
        <v-btn class="mt-2">Login</v-btn>
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
