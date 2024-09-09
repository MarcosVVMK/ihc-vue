<script>
export default {
  props: {
    currentStep: {
      type: Number,
      required: true,
      default: 1
    }
  },
  methods: {
    setStep(step) {
      this.$emit('update-step', step);
    }
  }
}
</script>

<template>
  <nav
      class="flex px-5 py-3 text-gray-700 rounded-lg bg-slate-100 dark:bg-gray-900 dark:border-gray-700"
      aria-label="Breadcrumb">
    <ol class="inline-flex items-center space-x-1 md:space-x-2 rtl:space-x-reverse">
      <li :class="['inline-flex items-center breadcrumbs-item', { 'active': currentStep === 1 }]" @click="setStep(1)">
        <a href="#"
           class="inline-flex items-center text-sm font-medium text-gray-700 hover:text-blue-600 dark:text-gray-400 dark:hover:text-white">
          Dados Pessoais
        </a>
      </li>
      <li :class="['breadcrumbs-item', { 'active': currentStep === 2 }]" @click="setStep(2)">
        <div class="flex items-center">
          <svg class="rtl:rotate-180 block w-3 h-3 mx-1 text-gray-400" aria-hidden="true"
               xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 6 10">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="m1 9 4-4-4-4"/>
          </svg>
          <a href="#"
             class="ms-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ms-2 dark:text-gray-400 dark:hover:text-white">
            Endereço
          </a>
        </div>
      </li>
      <li :class="['breadcrumbs-item', { 'active': currentStep === 3 }]" @click="setStep(3)" aria-current="page">
        <div class="flex items-center">
          <svg class="rtl:rotate-180 w-3 h-3 mx-1 text-gray-400" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
               fill="none" viewBox="0 0 6 10">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="m1 9 4-4-4-4"/>
          </svg>
          <a href="#"
             class="ms-1 text-sm font-medium text-gray-700 hover:text-blue-600 md:ms-2 dark:text-gray-400 dark:hover:text-white">
            Dados Hospitalares
          </a>
        </div>
      </li>
    </ol>
  </nav>
</template>

<style scoped>
.breadcrumbs-item {
  transition: transform 0.3s ease-in-out;
}

.breadcrumbs-item.active {
  transform: scale(1.1);
}

.breadcrumbs-item:hover {
  cursor: pointer;
}

.breadcrumbs-item.active a {
  color: black;
}

.dark .breadcrumbs-item.active a {
  color: white;
}

</style>