<script>
export default {
  name: 'PersonalInformationForm'
};
</script>

<template>
  <form class="max-w-md mx-auto" autocomplete="off">
    <h2 class="text-2xl font-semibold text-gray-900 dark:text-white p-6 text-center">Informações Pessoais</h2>

    <!-- Campo Nome -->
    <div class="relative z-0 w-full mb-5 group">
      <input type="text" name="nome" id="nome"
        class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
        placeholder=" " required autocomplete="off" />
      <label for="nome"
        class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Nome</label>
    </div>

    <!-- Campos Idade e Sexo na mesma linha -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <input type="number" name="idade" id="idade" min="0"
          class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
          placeholder=" " required autocomplete="off" />
        <label for="idade"
          class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Idade</label>
      </div>

      <div class="relative z-0 w-1/2 group">
        <input type="number" step="0.01"  name="peso" id="peso" min="0"
          class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
          placeholder=" " required autocomplete="off" />
        <label for="peso"
          class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Peso</label>
      </div>

      <div class="relative z-0 w-1/2 group">
        <input type="number" step="0.01" name="altura" id="altura" min="0"
          class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
          placeholder=" " required autocomplete="off" />
        <label for="altura"
          class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Altura
          (m)</label>
      </div>
      
    </div>

    <!-- Campos Altura e Raça/Cor na mesma linha -->
    <div class="flex space-x-4 mb-5">
      
      <div class="relative z-0 w-1/2 group">
        <select name="sexo" id="sexo"
          class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
          required autocomplete="off">
          <option value="" disabled selected class="bg-sky-300 dark:bg-gray-900"></option>
          <option value="masculino" class="bg-sky-300 dark:bg-gray-900">Masculino</option>
          <option value="feminino" class="bg-sky-300 dark:bg-gray-900">Feminino</option>
          <option value="outro" class="bg-sky-300 dark:bg-gray-900">Outro</option>
        </select>
        <label for="sexo"
          class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Sexo</label>
      </div>
      <div class="relative z-0 w-1/2 group">
        <select name="raca_cor" id="raca_cor"
          class="block py-2.5 px-0 w-full text-sm text-gray-900 bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600 peer"
          required autocomplete="off">
          <option value="" disabled selected class="bg-sky-300 dark:bg-gray-900"></option>
          <option value="branca" class="bg-sky-300 dark:bg-gray-900">Branca</option>
          <option value="preta" class="bg-sky-300 darkbg-gray-900">Preta</option>
          <option value="parda" class="bg-sky-300 dark:bg-gray-900">Parda</option>
          <option value="indigena" class="bg-sky-300 dark:bg-gray-900">Indígena</option>
          <option value="outros" class="bg-sky-300 dark:bg-gray-900">Outros</option>
        </select>
        <label for="raca_cor"
          class="peer-focus:font-medium absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Raça/Cor</label>
      </div>
    </div>
  </form>
</template>

<style scoped></style>