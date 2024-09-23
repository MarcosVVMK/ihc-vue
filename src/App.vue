<script setup>
import { ref, watch } from 'vue';
import Header from './components/partials/Header.vue';
import Forms from './components/partials/Forms.vue';
import Footer from './components/partials/Footer.vue';
import ServiceNumber from './components/partials/ServiceNumber.vue';
import { set } from '@vueuse/core';

const currentStep = ref(1);
const submitForm = ref(false);
const showServiceNumber = ref(false);

const updateStep = (newStep) => {
  currentStep.value = newStep;
  submitForm.value = false;
  showServiceNumber.value = false;

};

const updateSubmitForm = (submit) => {
  submitForm.value = submit;
  if (!submit) {
    showServiceNumber.value = submit;
  }
};

watch(submitForm, (newValue) => {
  if (newValue) {
    setTimeout(() => {
      submitForm.value = newValue;
      showServiceNumber.value = newValue;
    }, 1000); // Simule uma operação assíncrona de 1 segundo
  }
});

const lightSwitches = document.querySelectorAll('.light-switch');
if (lightSwitches.length > 0) {
  lightSwitches.forEach((lightSwitch, i) => {
    if (localStorage.getItem('dark-mode') === 'true') {
      lightSwitch.checked = true;
    }
    lightSwitch.addEventListener('change', () => {
      const { checked } = lightSwitch;
      lightSwitches.forEach((el, n) => {
        if (n !== i) {
          el.checked = checked;
        }
      });
      if (lightSwitch.checked) {
        document.documentElement.classList.add('dark');
        localStorage.setItem('dark-mode', true);
      } else {
        document.documentElement.classList.remove('dark');
        localStorage.setItem('dark-mode', false);
      }
    });
  });
}
</script>

<template>
  <section class="flex flex-col h-screen overflow-hidden bg-slate-100 dark:bg-gray-900">
    <Header :currentStep="currentStep" @update-step="updateStep" />
    <main class="flex-grow flex items-center justify-center">
      <ServiceNumber v-if="showServiceNumber" />
      <Forms v-else :currentStep="currentStep" />
    </main>
    <Footer :currentStep="currentStep" @update-step="updateStep" :submitForm="submitForm" @update-submit-form="updateSubmitForm" />
  </section>
</template>

<style scoped>
</style>