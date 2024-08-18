<script>
import PersonalInformationForm from '../forms/PersonalInformationForm.vue'
import ServiceInformationForm from '../forms/ServiceInformationForm.vue'

export default {
  components: {
    PersonalInformationForm,
    ServiceInformationForm
  },
  props: {
    currentStep: {
      //type: Number,
      type: 1,
      required: true
    }
  }
};
</script>

<template>
  <div>
    <div v-if="currentStep === 1">
      <PersonalInformationForm />
    </div>
    <div v-else-if="currentStep === 2">
      <ServiceInformationForm />
    </div>
  </div>
</template>

<style scoped>
</style>