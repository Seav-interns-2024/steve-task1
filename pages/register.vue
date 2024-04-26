<template>
  <v-container class="bg-grey-lighter min-h-screen d-flex flex-column">
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="6">
        <v-card class="rounded shadow-xl">
          <v-card-title class="mb-8 text-center font-bold">
            <h1 class="text-3xl">Sign up</h1>
          </v-card-title>
          <v-card-text>
            <v-form @submit.prevent="submitForm">

              <v-text-field v-model="formData.fullname" label="Full Name" required outlined class="mb-4"
                dense></v-text-field>

              <v-text-field v-model="formData.email" label="Email" required outlined class="mb-4" dense></v-text-field>

              <v-text-field v-model="formData.password" label="Password" required outlined class="mb-4" dense
                type="password"></v-text-field>

              <v-text-field v-model="formData.passwordconfirmation" label="Confirm Password" required outlined
                class="mb-4" dense type="password"></v-text-field>

              <v-btn type="submit" class="rounded mx-auto" color="green" dark block>
                Create Account
              </v-btn>

              <div class="text-center text-sm text-grey-dark mt-4 font-medium">
                By signing up, you agree to the
                <a class="no-underline border-b border-grey-dark text-grey-dark">Terms of Service</a>
                and
                <a class="no-underline border-b border-grey-dark text-grey-dark">Privacy Policy</a>
              </div>
            </v-form>
          </v-card-text>
        </v-card>
        <div class="text-center text-grey-dark mt-10 font-medium">
          Already have an account?
          <a @click="login" class="underline border-b border-blue text-blue" href="login">Log in</a>.
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    const formData = reactive({
      address: null,
      fullname: '',
      email: '',
      password: '',
      passwordconfirmation: ''
    });

    const submitForm = () => {
      console.log('Form submitted:', formData);
    };

    const login = () => {
      alert('Go to login page');
    };

    return {
      formData,
      submitForm,
      login,
    };
  }
};

</script>

<style scoped>
.container {
  max-width: 1200px;
  padding-left: 20px;
  padding-right: 20px;
}

@media (max-width: 768px) {
  .container {
    width: 100%;
  }
}
</style>
