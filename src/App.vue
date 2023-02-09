<template>
  <v-app>
    <NavBar />
    <v-main>
      <v-container fluid>
        <RouterView />
      </v-container>
    </v-main>
    <v-footer> footer </v-footer>
  </v-app>
</template>
<script setup lang="ts">
import { RouterView } from 'vue-router';
import NavBar from '@/components/layouts/NavBar.vue';
</script>
