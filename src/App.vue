<script setup lang="ts">
import ThemeProvider from '@/providers/ThemeProvider.vue';
import { RouterView } from 'vue-router';

</script>

<template>
  <ThemeProvider>
    <RouterView />
  </ThemeProvider>
</template>

<style scoped></style>
