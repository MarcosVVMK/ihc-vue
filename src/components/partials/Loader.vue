<script setup>
import { useLoader } from '../../composables/UseLoader.js';

const { isLoading } = useLoader();
</script>

<template>
  <div v-if="isLoading" class="fixed inset-0 flex items-center justify-center bg-gray-900 bg-opacity-50 z-50">
    <div class="loader"></div>
  </div>
</template>

<style scoped>
.loader {
  border: 4px solid rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  border-top: 4px solid white;
  width: 40px;
  height: 40px;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
</style>