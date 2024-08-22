<script setup>
import { defineEmits } from 'vue';

const emit = defineEmits(['update-step']);

function updateStep() {
  emit('update-step', 1);
}
</script>

<template>
  <div class="flex items-center cursor-pointer" @click="updateStep">
    <img src="../../assets/images/logo.png" alt="Logo" class="w-12 h-12" />
    <span class="text-black dark:text-white text-2xl font-bold ml-2">SIGH</span>
  </div>
</template>

<style scoped>
</style>