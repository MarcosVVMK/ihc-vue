<script>
export default {
  name: 'PersonalInformationForm'
};
</script>

<template>
  <form class="max-w-4xl mx-auto min-h-screen text-lg" autocomplete="off">
    <h2 class="text-2xl font-semibold text-gray-900 dark:text-white p-6 text-center">Informações Pessoais</h2>

    <!-- Campo Nome -->
    <div class="relative z-0 w-full mb-5 group">
      <label for="nome" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Nome</label>
      <input type="text" name="nome" id="nome"
             class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
             placeholder="Digite seu nome completo" required autocomplete="off" />
    </div>

    <!-- Campos Idade e Peso na mesma linha -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <label for="idade" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Idade</label>
        <input type="number" name="idade" id="idade" min="0"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite sua idade" required autocomplete="off" />
      </div>

      <div class="relative z-0 w-1/2 group">
        <label for="peso" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Peso</label>
        <input type="number" step="0.01" name="peso" id="peso" min="0"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite seu peso (kg)" required autocomplete="off" />
      </div>
    </div>

    <!-- Campos Altura e Sexo na mesma linha -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <label for="altura" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Altura (m)</label>
        <input type="number" step="0.01" name="altura" id="altura" min="0"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite sua altura (m)" required autocomplete="off" />
      </div>

      <div class="relative z-0 w-1/2 group">
        <label for="sexo" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Sexo</label>
        <select name="sexo" id="sexo"
                class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
                required autocomplete="off">
          <option value="" disabled selected class="bg-slate-100 dark:bg-gray-900">Selecione seu sexo</option>
          <option value="masculino" class="bg-slate-100 dark:bg-gray-900">Masculino</option>
          <option value="feminino" class="bg-slate-100 dark:bg-gray-900">Feminino</option>
          <option value="outro" class="bg-slate-100 dark:bg-gray-900">Outro</option>
        </select>
      </div>
    </div>

    <!-- Campo Raça/Cor -->
    <div class="relative z-0 w-full mb-5 group">
      <label for="raca_cor" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Raça/Cor</label>
      <select name="raca_cor" id="raca_cor"
              class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
              required autocomplete="off">
        <option value="" disabled selected class="bg-slate-100 dark:bg-gray-900">Selecione sua raça/cor</option>
        <option value="branca" class="bg-slate-100 dark:bg-gray-900">Branca</option>
        <option value="preta" class="bg-slate-100 dark:bg-gray-900">Preta</option>
        <option value="parda" class="bg-slate-100 dark:bg-gray-900">Parda</option>
        <option value="indigena" class="bg-slate-100 dark:bg-gray-900">Indígena</option>
        <option value="outros" class="bg-slate-100 dark:bg-gray-900">Outros</option>
      </select>
    </div>
  </form>
</template>

<style scoped>
/* Adicione estilos personalizados aqui, se necessário */
</style>