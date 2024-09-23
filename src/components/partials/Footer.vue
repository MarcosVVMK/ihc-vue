<script>
import NextButton from '../buttons/NextButton.vue';
import PreviousButton from '../buttons/PreviousButton.vue';
import SubmitButton from '../buttons/SubmitButton.vue';

export default {
  name: 'Footer',
  components: {
    NextButton,
    PreviousButton,
    SubmitButton
  },
  props: {
    currentStep: {
      type: Number,
      required: true
    },
    submitForm: {
      type: Boolean,
      required: true,
      default: false
    }
  },
  methods: {
    nextStep() {
      this.$emit('update-step', this.currentStep + 1);
    },
    previousStep() {
      
      if ( this.submitForm ){
        this.$emit('update-step', this.currentStep - 0);

      }else{
        this.$emit('update-step', this.currentStep - 1);
      }

      this.$emit('update-submit-form', false);
      this.submitForm = false;
    },
    handleSubmit() {
      this.$emit( 'update-submit-form', true);
    }
  }
};
</script>

<template>
  <footer class="footer bg-slate-100 dark:bg-gray-900">
    <div class="flex justify-between items-center">
      <PreviousButton v-if="currentStep > 1" @previous-step="previousStep" @revert-submit="revertSubmit"/>
      <div class="ml-auto">
        <NextButton v-if="currentStep < 3" @next-step="nextStep" />
        <SubmitButton v-if="currentStep === 3 && !submitForm" @handle-submit="handleSubmit"/>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  padding: 2rem; /* Espaçamento interno */
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.2); /* Sombra para criar divisão */
  z-index: 1000; /* Certifique-se de que o footer esteja acima de outros elementos */
}
</style>