<script setup>
import { ref } from 'vue';
import Header from './components/partials/Header.vue';
import Forms from './components/partials/Forms.vue';
import Footer from './components/partials/Footer.vue';

const currentStep = ref(1);

const updateStep = (newStep) => {
  currentStep.value = newStep;
};
</script>

<template>
  <section class="flex-grow bg-gray-900 min-h-screen">
    <Header :currentStep="currentStep" @update-step="updateStep" />
    <main class="flex-grow">
      <Forms :currentStep="currentStep" />
    </main>
    <Footer :currentStep="currentStep" @update-step="updateStep" />
  </section>
</template>

<style scoped>
</style>