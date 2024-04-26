<template>
  <div class="text-overlay text-white text-9xl font-serif">
    <h2>Stanford</h2>
  </div>
  <v-img src="assets/standford.jpg" cover height="fixed" />
  <v-footer color="transparent">
    <v-row justify="center" no-gutters>
      <v-btn v-for="link in links" :key="link" class="mx-2" color="black" rounded="x1" variant="text">
        {{ link }}
      </v-btn>
      <v-col class="text-center mt-4" cols="12">
        {{ new Date().getFullYear() }} — <strong>Stanford</strong>
      </v-col>
    </v-row>
  </v-footer>

</template>

<script setup lang="ts">
import { defineProps, ref } from 'vue';

const props = defineProps({
  links: {
    type: Array as () => string[],
    required: true,
  },
});

const sheet = ref(false);
const links = [
  'News',
  'Events',
  'Academics',
  'Research',
  'Health Care',
  'Admission',
];
</script>



<style scoped>
.text-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  z-index: 1;
}

.text-overlay h1 {
  font-size: 36px;
}
</style>