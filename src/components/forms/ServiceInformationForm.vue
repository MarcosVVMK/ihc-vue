<script>
export default {
  name: 'ServiceInformationForm',
  props: {
    showForm: {
      type: Boolean,
      required: true,
    },
    showLoader: {
      type: Boolean,
      required: true,
    }
  },
};
</script>

<template>
  <form class="max-w-4xl mx-auto min-h-screen text-lg" autocomplete="off">
    <h2 class="text-2xl font-semibold text-gray-900 dark:text-white p-6 text-center">Informações de Serviço</h2>

    <!-- Campo Plano de Saude e Matrícula do Plano -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <label for="planoSaude" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Plano de Saude</label>
        <input type="text" name="planoSaude" id="planoSaude"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite o plano de saúde" required autocomplete="off" />
      </div>
      <div class="relative z-0 w-1/2 group">
        <label for="matriculaPlano" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Matrícula do Plano</label>
        <input type="text" name="matriculaPlano" id="matriculaPlano"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite a matrícula do plano" required autocomplete="off" />
      </div>
    </div>

    <!-- Campo Vencimento da carteirinha do plano e Senha do painel -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <label for="vencimentoCarteirinha" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Vencimento da carteirinha</label>
        <input type="date" name="vencimentoCarteirinha" id="vencimentoCarteirinha"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite o vencimento da carteirinha" required autocomplete="off" />
      </div>
      <div class="relative z-0 w-1/2 group">
        <label for="senhaPainel" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Senha do painel</label>
        <input type="text" name="senhaPainel" id="senhaPainel"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite a senha do painel" required autocomplete="off" />
      </div>
    </div>

    <!-- Campo Data do atendimento e Hora do atendimento -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <label for="dataAtendimento" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Data do atendimento</label>
        <input type="date" name="dataAtendimento" id="dataAtendimento"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite a data do atendimento" required autocomplete="off" />
      </div>
      <div class="relative z-0 w-1/2 group">
        <label for="horaAtendimento" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Hora do atendimento</label>
        <input type="time" name="horaAtendimento" id="horaAtendimento"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite a hora do atendimento" required autocomplete="off" />
      </div>
    </div>
  </form>
</template>

<style scoped>
/* Adicione estilos personalizados aqui, se necessário */
</style>