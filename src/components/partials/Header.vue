<script>
export default {
  props: {
    currentStep: {
      type: Number,
      required: true,
      default: 1
    }
  }
};
import BreadCrumb from './Breadcrumbs.vue'
import DarkModeToggle from './DarkModeToggle.vue'

</script>

<template>
  <header class="bg-gray-900 p-16">
    <div class="flex flex-col items-center mb-4">
      <h1 class="text-white text-2xl font-bold mb-2">SIGH - Sistema de Gerenciamento Hospitalar</h1>
    </div>
    <Breadcrumbs :currentStep="currentStep" />
  </header>
</template>

<style scoped>
</style>