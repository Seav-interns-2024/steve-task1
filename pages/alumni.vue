<template>
   <div class="flex-1 flex-col justify-center px-6 py-5 lg:px-8">
      <div class="sm:mx-auto sm:w-full sm:max-w-sm">
         <img class="mb-4" src="assets/stanford-university-logo.webp" alt="Your Company" />
         <h2 class="mt-3 text-center text-2xl font-bold leading-5 tracking-tight text-gray-900">Sign in to your account
         </h2>
      </div>
   </div>

   <form>
      <div>
         <div class="bg-white px-4 rounded shadow-md text-black w-full">
            <form @submit.prevent="submitForm">
               <div class="mb-4">
                  <label class="block text-gray-700 text-sm font-bold mb-2" for="username">Email:</label>
                  <input
                     class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                     type="text" id="username" v-model="formData.username">
               </div>
               <div class="mb-4">
                  <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                     Password
                  </label>
               </div>
               <input
                  class="shadow appearance-none border border-red-500 rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline"
                  id="password" type="password" placeholder="************">
               <p class="text-red-500 text-xs italic">Enter your password.</p>

               <div class="flex items-center justify-between">
                  <button @click="Done"
                     class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 focus:outline-none focus:shadow-outline"
                     type="submit">
                     Sign In
                  </button>
                  <a @click="Forgot" class="inline-block align-baseline font-bold text-sm text-blue-500 hover:text-blue-800" href="">
                     Forgot Password?
                  </a>
               </div>
            </form>
         </div>
      </div>
   </form>
</template>

<script>
export default {
   data() {
      return {
         formData: {
            username: '',
            password: ''
         }
      }
   },
   methods: {
      submitForm() {
         console.log('Form submitted:', this.formData);

      },
      Forgot() {
         alert('Kindly reset your password')
      },
      Done() {
         alert('Well done, you in!')
      }
   }
};

</script>