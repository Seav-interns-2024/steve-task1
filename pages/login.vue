<template>
   <v-container>
      <v-row justify="center">
         <v-col cols="12" sm="8" md="6">
            <v-card class="elevation-10">
               <v-img src="c:\Users\ANDREW\first-project\Admission\assets\SUlogo.webp" alt="Your Company"
                  class="mx-auto mt-8"></v-img>
               <v-card-title class="text-center text-xl font-bold">
                  Sign in to your account
               </v-card-title>
               <v-card-text>
                  <v-form @submit.prevent="submitForm">
                     <v-text-field v-model="formData.username" label="Email" outlined hide-details="auto"
                        class="mb-4"></v-text-field>
                     <v-text-field v-model="formData.password" label="Password" type="password" outlined
                        hide-details="auto" class="mb-4"></v-text-field>
                     <v-btn type="submit" color="primary" block>Sign In</v-btn>
                  </v-form>
               </v-card-text>
               <v-divider class="my-6"></v-divider>
               <v-card-actions>
                  <v-btn text @click="forgotPassword" class="mx-auto" href="register">Forgot Password?</v-btn>
               </v-card-actions>
            </v-card>
         </v-col>
      </v-row>
   </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const formData = ref({
   username: '',
   password: ''
});

const submitForm = (): void => {
   console.log('Form submitted:', formData.value);
   formData.value.username = '';
   formData.value.password = '';
};

const forgotPassword = (): void => {
   alert('Kindly reset your password');
};
</script>


<style scoped>
.elevation-10 {
   box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2);
}
</style>
