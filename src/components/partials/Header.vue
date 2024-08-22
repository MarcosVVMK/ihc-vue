<script>
import Breadcrumbs from "./Breadcrumbs.vue";
import DarkModeToggle from "./DarkModeToggle.vue";
import Logo from "./Logo.vue";

export default {
  components: {Logo, Breadcrumbs, DarkModeToggle },
  props: {
    currentStep: {
      type: Number,
      required: true,
      default: 1
    }
  }
};
</script>
<template>
  <header class="bg-teal-300 dark:bg-gray-900 p-16 header-container">
    <div class="logo-container">
      <Logo :currentStep="currentStep" @update-step="$emit('update-step', $event)"  />
    </div>
    <div class="flex flex-col items-center mb-4">
      <h1 class="text-black dark:text-white text-2xl font-bold mb-2">Sistema de Gerenciamento Hospitalar</h1>
    </div>
    <div class="breadcrumbs-container">
      <Breadcrumbs :currentStep="currentStep" @update-step="$emit('update-step', $event)" />
    </div>
    <div class="darkmode-toggle-container">
      <DarkModeToggle />
    </div>
  </header>
</template>
<style scoped>
.breadcrumbs-container {
  max-width: 28rem;
  margin: 0 auto;
}

.header-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.darkmode-toggle-container {
  position: absolute;
  top: 1rem;
  right: 1rem;
}
.logo-container{
  position: absolute;
  top: 1rem;
  left: 4rem;
}
</style>