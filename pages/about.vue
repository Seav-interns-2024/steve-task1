<template>
  <v-card>
    <v-tabs
      v-model="tab"
      align-tabs="end"
      color="deep-purple-accent-4"
    >
      <v-tab :value="1">Events</v-tab>
      <v-tab :value="2">Academics</v-tab>
      <v-tab :value="3">Research</v-tab>
    </v-tabs>
    <v-window v-model="tab">
      <v-window-item
        v-for="n in 3"
        :key="n"
        :value="n"
      >
        <v-container fluid>
          <v-row>
            <v-col
              v-for="i in 6"
              :key="i"
              cols="12"
              md="4"
            >
              <v-img
                :lazy-src="`https://picsum.photos/10/6?image=${i * n * 5 + 10}`"
                :src="`https://picsum.photos/500/300?image=${i * n * 5 + 10}`"
                aspect-ratio="1"
              ></v-img>
            </v-col>
          </v-row>
        </v-container>
      </v-window-item>
    </v-window>
  </v-card>
</template>
<script lang="ts">
  import { defineComponent, ref } from 'vue';

  export default defineComponent({
    data() {
      return {
        tab: null as null | string,
      };
    },
  });
</script>
