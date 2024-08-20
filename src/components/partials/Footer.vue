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
    }
  },
  methods: {
    nextStep() {
      this.$emit('update-step', this.currentStep + 1);
    },
    previousStep() {
      this.$emit('update-step', this.currentStep - 1);
    }
  }
};
</script>

<template>
  <footer class="footer">
    <div class="flex justify-between items-center">
      <PreviousButton v-if="currentStep > 1" @previous-step="previousStep" />
      <div class="ml-auto">
        <NextButton v-if="currentStep < 3" @next-step="nextStep" />
        <SubmitButton v-if="currentStep === 3" />
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #1a202c; /* Cor de fundo cinza escuro */
  padding: 2rem; /* Espaçamento interno */
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.2); /* Sombra para criar divisão */
  z-index: 1000; /* Certifique-se de que o footer esteja acima de outros elementos */
}
</style>