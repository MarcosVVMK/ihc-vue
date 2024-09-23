<script>
export default {
  name: 'AddressInformationForm'
};
</script>

<template>
  <form class="max-w-4xl mx-auto min-h-screen text-lg" autocomplete="off">
    <h2 class="text-2xl font-semibold text-gray-900 dark:text-white p-6 text-center">Informações de Contato</h2>

    <!-- Campo Telefone -->
    <div class="relative z-0 w-full mb-5 group">
      <label for="telefone" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Telefone</label>
      <input type="tel" name="telefone" id="telefone"
             class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
             placeholder="Digite seu telefone" required autocomplete="off" />
    </div>

    <!-- Campos Endereço e CEP na mesma linha -->
    <div class="flex space-x-4 mb-5">
      <div class="relative z-0 w-1/2 group">
        <label for="endereco" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Endereço</label>
        <input type="text" name="endereco" id="endereco"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite seu endereço" required autocomplete="off" />
      </div>
      <div class="relative z-0 w-1/2 group">
        <label for="cep" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">CEP</label>
        <input type="text" name="cep" id="cep"
               class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
               placeholder="Digite seu CEP" required autocomplete="off" />
      </div>
    </div>

    <!-- Campo Pai -->
    <div class="relative z-0 w-full mb-5 group">
      <label for="pai" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Pai</label>
      <input type="text" name="pai" id="pai"
             class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
             placeholder="Digite o nome do pai" required autocomplete="off" />
    </div>

    <!-- Campo Mãe -->
    <div class="relative z-0 w-full mb-5 group">
      <label for="mae" class="block text-lg text-gray-500 dark:text-gray-400 mb-2">Mãe</label>
      <input type="text" name="mae" id="mae"
             class="block py-2.5 px-0 w-full text-lg text-gray-900 bg-transparent border-0 border-b-2 border-gray-400 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-blue-500 focus:outline-none focus:ring-0 focus:border-blue-600"
             placeholder="Digite o nome da mãe" required autocomplete="off" />
    </div>
  </form>
</template>

<style scoped>
/* Adicione estilos personalizados aqui, se necessário */
</style>