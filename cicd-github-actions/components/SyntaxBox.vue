<template>
  <div class="bg-purple-50 border-l-4 border-purple-500 p-4 rounded-r-lg dark:bg-purple-900/30 dark:border-purple-400">
    <h3 class="text-purple-700 font-bold text-lg mb-3 dark:text-purple-300">🚀 Sintaxis y parámetros</h3>
    
    <div class="bg-gray-900 text-green-400 p-3 rounded font-mono text-sm mb-4 dark:bg-gray-800 dark:text-green-300">
      {{ command }}
    </div>
    
    <div class="space-y-2">
      <div 
        v-for="param in parameters" 
        :key="param.name"
        class="flex items-start"
      >
        <span class="text-purple-600 font-mono text-sm bg-purple-100 px-2 py-1 rounded mr-3 dark:text-purple-300 dark:bg-purple-800/50">
          {{ param.name }}
        </span>
        <span class="text-purple-800 text-sm dark:text-purple-200" v-html="param.description"></span>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  command: String,
  parameters: Array
})
</script>