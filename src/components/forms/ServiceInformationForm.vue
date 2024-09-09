<script>
export default {
  name: 'ServiceInformationForm'
};
</script>

<template>
  <form class="max-w-4xl mx-auto min-h-screen text-lg" autocomplete="off">
    <h2 class="text-2xl font-semibold text-gray-900 dark:text-white p-6 text-center">Informações de Serviço</h2>

    <!-- Campo Plano de Saude e Matrícula do Plano -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <input type="text" name="planoSaude" id="planoSaude"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
               placeholder=" " required autocomplete="off" />
        <label for="planoSaude"
               class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Plano de Saude</label>
      </div>
      <div class="relative z-0 w-1/2 group">
        <input type="text" name="matriculaPlano" id="matriculaPlano"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
               placeholder=" " required autocomplete="off" />
        <label for="matriculaPlano"
               class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Matrícula do Plano</label>
      </div>
    </div>

    <!-- Campo Vencimento da carteirinha do plano e Senha do painel -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <input type="date" name="vencimentoCarteirinha" id="vencimentoCarteirinha"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
               placeholder=" " required autocomplete="off" />
        <label for="vencimentoCarteirinha"
               class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Vencimento da carteirinha</label>
      </div>
      <div class="relative z-0 w-1/2 group">
        <input type="text" name="senhaPainel" id="senhaPainel"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
               placeholder=" " required autocomplete="off" />
        <label for="senhaPainel"
               class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Senha do painel</label>
      </div>
    </div>

    <!-- Campo Data do atendimento e Hora do atendimento -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <input type="date" name="dataAtendimento" id="dataAtendimento"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
               placeholder=" " required autocomplete="off" />
        <label for="dataAtendimento"
               class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Data do atendimento</label>
      </div>
      <div class="relative z-0 w-1/2 group">
        <input type="time" name="horaAtendimento" id="horaAtendimento"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
               placeholder=" " required autocomplete="off" />
        <label for="horaAtendimento"
               class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Hora do atendimento</label>
      </div>
    </div>

    <!-- Campo Número do Prontuario -->
    <div class="relative z-0 w-full mb-5 group">
      <input type="text" name="numeroProntuario" id="numeroProntuario"
             class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
             placeholder=" " required autocomplete="off" />
      <label for="numeroProntuario"
             class="peer-focus:font-medium absolute text-lg text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Número do Prontuario</label>
    </div>
  </form>
</template>

<style scoped>
</style>