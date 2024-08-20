<script>
import PersonalInformationForm from '../forms/PersonalInformationForm.vue';
import ServiceInformationForm from '../forms/ServiceInformationForm.vue';
import AddressInformationForm from '../forms/AddressInformationForm.vue';

export default {
  components: {
    PersonalInformationForm,
    ServiceInformationForm,
    AddressInformationForm
  },
  props: {
    currentStep: {
      type: Number,
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
      <AddressInformationForm />
    </div>
    <div v-else-if="currentStep === 3">
      <ServiceInformationForm />
    </div>
    
  </div>
</template>

<style scoped>
</style>