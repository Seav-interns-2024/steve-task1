<template>
  <v-card>
    <v-layout>
      <v-app-bar class="transparent">
        <NuxtLink to="/" class="font-serif font-extrabold m-5 h-6 text-xl text-red-400">Stanford University</NuxtLink>
        <v-spacer></v-spacer>
        <v-app-bar-nav-icon variant="text" class="max-h-9" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <template v-if="$vuetify.display.mdAndUp">
        </template>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" :location="$vuetify.display.mobile ? 'bottom' : 'right'" temporary
        color="transparent">
        <NuxtLink to="/register" @click="handleClick('Register', '/register')">
          <v-list-item title="Register"></v-list-item>
        </NuxtLink>
        <NuxtLink to="/login" @click="handleClick('Login', '/login')">
          <v-list-item title="Login"></v-list-item>
        </NuxtLink>
        <NuxtLink to="/about" @click="handleClick('About', '/about')">
          <v-list-item title="About"></v-list-item>
        </NuxtLink>
      </v-navigation-drawer>
      <v-main>
        <slot />
      </v-main>
    </v-layout>
  </v-card>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useRoute } from 'vue-router';

const drawer = ref(false);
const route = useRoute();

const handleClick = (name: string, link: string): void => {
  console.log(`name: ${name}, link: ${link}`);
};
</script>

<style scoped>
.transparent {
  background-color: transparent !important;
}
</style>
