<script setup>
import { ref, onMounted } from 'vue';

const serviceNumber = ref('');

function generateRandomNumber() {
  // Gera um número aleatório de 6 dígitos
  return Math.floor(100000 + Math.random() * 900000).toString();
}

onMounted(() => {
  serviceNumber.value = generateRandomNumber();
});

</script>

<template>
  <div class="justify-center h-screen bg-slate-100 dark:bg-gray-900">
    <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-lg">
      <h1 class="text-4xl font-bold mb-4 text-gray-900 dark:text-white text-center">Número do Prontuário</h1>
      <h1 class="text-9xl text-gray-700 dark:text-gray-300">{{ serviceNumber }}</h1>
    </div>
  </div>
</template>

<style scoped>
</style>