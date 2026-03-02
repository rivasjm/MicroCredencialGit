<template>
  <div class="flex items-center bg-white dark:bg-gray-900 border-l-4 border-purple-500 rounded-lg shadow-md p-2 gap-2">
    <div class="flex flex-col justify-center">
      <div class="font-bold text-base text-purple-700 dark:text-purple-300 mb-0.5">{{ titulo }}</div>
      <div class="text-xs text-gray-700 dark:text-gray-200 mb-0.5">
        {{ autor }}
        <span v-if="año"> ({{ año }})</span>
        <span v-if="edicion" class="ml-1 px-1 py-0.5 bg-purple-100 text-purple-700 rounded text-xs">{{ edicion }}</span>
      </div>
      <div v-if="capitulo" class="text-xs text-gray-500 dark:text-gray-400 italic">Capítulo: {{ capitulo }}</div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  titulo: { type: String, required: true },
  autor: { type: String, required: true },
  año: { type: [String, Number], default: '' },
  edicion: { type: String, default: '' },
  capitulo: { type: String, default: '' }
})
</script>
