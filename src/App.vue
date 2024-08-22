<script setup>
import { ref } from 'vue';
import Header from './components/partials/Header.vue';
import Forms from './components/partials/Forms.vue';
import Footer from './components/partials/Footer.vue';

const currentStep = ref(1);

const updateStep = (newStep) => {
  currentStep.value = newStep;
};

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
  <section class="flex-grow bg-sky-300 dark:bg-gray-900 min-h-screen">
    <Header :currentStep="currentStep" @update-step="updateStep" />
    <main class="flex-grow">
      <Forms :currentStep="currentStep" />
    </main>
    <Footer :currentStep="currentStep" @update-step="updateStep" />
  </section>
</template>

<style scoped>
</style>