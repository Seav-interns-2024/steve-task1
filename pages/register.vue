<template>
  <div class="bg-grey-lighter min-h-screen flex flex-col">
    <div class="container max-w-sm mx-auto flex-1 flex flex-col items-center justify-center px-2">
      <div class="bg-white px-4 rounded shadow-md text-black w-full">
        <h1 class="mb-8 text-3xl text-center font-bold ">Sign up</h1>
        <div>
          <form @submit.prevent="submitForm">
            <input type="text" class="block border border-grey-light w-full p-3 rounded mb-4" required
              v-model="formData.fullname" placeholder="Full Name" />

            <input type="text" class="block border border-grey-light w-full p-3 rounded mb-4" required
              v-model="formData.email" placeholder="Email" />

            <input type="password" class="block border border-grey-light w-full p-3 rounded mb-4" required
              v-model="formData.password" placeholder="Password" />
            <input type="password" class="block border border-grey-light w-full p-3 rounded mb-4" required
              v-model="formData.password" placeholder="Confirm Password" />

            <button type="submit"
              class="w-full text-center  rounded bg-green text-white hover:bg-green-dark focus:outline-none my-1">Create
              Account</button>

            <div class="text-center text-sm text-grey-dark mt-4 font-medium">
              By signing up, you agree to the
              <a class="no-underline border-b border-grey-dark text-grey-dark" href="#">
                Terms of Service
              </a> and
              <a class="no-underline border-b border-grey-dark text-grey-dark" href="#">
                Privacy Policy
              </a>
            </div>
          </form>
        </div>
      </div>
      <div class="text-grey-dark mt-10 font-medium">
        Already have an account?
        <a class="underline border-b border-blue text-blue" href="../login/">
          Log in
        </a>.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        email: '',
        password: ''
      }

    }
  },
  methods: {
    submitForm() {
      console.log('Form submitted:', this.formData);
    }
  }
}

</script>

<style>
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}

label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}

input,
select {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid;
  color: #555;
}

input[type="checkbox"] {
  display: inline-block;
  width: 16px;
  margin: 0 10px 0 0;
  position: relative;
  top: 2px;
}

.pill {
  display: inline-block;
  margin: 20px 10px 0 0;
  padding: 6px 12px;
  background: #eee;
  border-radius: 20px;
  font-size: 12px;
  letter-spacing: 1px;
  font-weight: bold;
  color: #777;
  cursor: pointer;
}

button {
  background: #0b6dff;
  border: 0;
  padding: 10px 20px;
  margin-top: 20px;
  color: white;
  border-radius: 20px;
}

.submit {
  text-align: center;
}

.error {
  color: #ff0000;
  margin-top: 10px;
  font-size: 0.8em;
  font-weight: bold;
}

.container {
  /* Set a maximum width for the container */
  max-width: 1200px;
  /* Adjust this value as needed */

  /* Add some padding to the sides */
  padding-left: 20px;
  padding-right: 20px;
}

/* Media query for smaller screens */
@media (max-width: 768px) {
  .container {
    /* Expand the container to take up the entire width */
    width: 100%;
  }
}
</style>
