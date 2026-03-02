<template>
  <div class="grid grid-cols-[1fr_2fr_2fr] gap-x-8 items-center mt-6">
    
    <!-- Headers -->
    <div></div>
    <div class="text-center font-bold mb-2 text-gray-700 dark:text-gray-300 text-sm" v-html="firstColumnTitle"></div>
    <div v-click="clickStep" class="text-center font-bold mb-2 text-gray-700 dark:text-gray-300 text-sm" v-html="secondColumnTitle"></div>

    <!-- Remote Repository -->
    <div class="text-blue-600 dark:text-blue-400 font-bold text-center text-sm">🌐 Repositorio Remoto</div>
    
    <div class="bg-blue-50 dark:bg-blue-950 border-2 border-blue-200 dark:border-blue-700 p-2 rounded-lg shadow-md w-fit mx-auto">
      <div class="flex justify-center">
        <slot name="remote-before"></slot>
      </div>
    </div>
    
    <div v-click="clickStep" class="bg-blue-50 dark:bg-blue-950 border-2 border-blue-200 dark:border-blue-700 p-2 rounded-lg shadow-md w-fit mx-auto">
      <div class="flex justify-center">
        <slot name="remote-after"></slot>
      </div>
    </div>

    <!-- Local Repository -->
    <div class="text-green-600 dark:text-green-400 font-bold text-center mt-3 text-sm">💻 Repositorio Local</div>
    
    <div v-if="localBefore === null" class="bg-green-50 dark:bg-green-950 border-2 border-green-200 dark:border-green-700 p-2 rounded-lg shadow-md w-fit mx-auto mt-3 flex items-center justify-center min-h-[80px]">
      <div class="text-center text-gray-500 dark:text-gray-400 italic text-sm">
        ❌ No existe repositorio local
      </div>
    </div>
    <div v-else class="bg-green-50 dark:bg-green-950 border-2 border-green-200 dark:border-green-700 p-2 rounded-lg shadow-md w-fit mx-auto mt-3">
      <div class="flex justify-center">
        <slot name="local-before"></slot>
      </div>
    </div>
    
    <div v-click="clickStep" class="bg-green-50 dark:bg-green-950 border-2 border-green-200 dark:border-green-700 p-2 rounded-lg shadow-md w-fit mx-auto mt-3">
      <div class="flex justify-center">
        <slot name="local-after"></slot>
      </div>
    </div>

  </div>

  <div v-if="note" v-click="clickStep" :class="noteClass">
    <span v-html="note"></span>
  </div>
</template>

<script setup>
defineProps({
  firstColumnTitle: { type: String, default: 'Situación inicial' },
  secondColumnTitle: { type: String, default: 'Después del comando' },
  localBefore: { type: [String, null], default: '' },
  clickStep: { type: Number, default: 1 },
  note: { type: String, default: '' },
  noteClass: { 
    type: String, 
    default: 'absolute bottom-5 right-5 bg-blue-100 dark:bg-blue-900 border-l-4 border-blue-500 dark:border-blue-400 text-blue-700 dark:text-blue-300 p-4 rounded shadow-lg max-w-xs text-sm z-10' 
  }
})
</script>