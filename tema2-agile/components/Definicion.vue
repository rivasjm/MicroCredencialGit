<template>
  <div class="relative bg-gradient-to-r from-blue-50 to-indigo-50 border-l-4 border-blue-500 p-6 rounded-lg shadow-xl max-w-2xl mx-auto my-6 transform hover:scale-105 transition-transform duration-300">
    
    <!-- Header with emoji and title -->
    <div class="flex items-center gap-4 mb-4">
      <div v-if="emoji" class="bg-white rounded-full p-2 shadow-md">
        <span class="text-3xl">{{ emoji }}</span>
      </div>
      <div class="flex-1">
        <span class="font-bold text-xl text-blue-800 tracking-wide">
          {{ title }}
        </span>
        <div class="h-1 w-full bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full mt-1"></div>
      </div>
    </div>
    
    <!-- Content -->
    <div class="text-gray-700 text-lg leading-relaxed">
      <slot />
    </div>
    
    <!-- Subtle background pattern -->
    <div class="absolute inset-0 opacity-5 pointer-events-none">
      <div class="absolute top-4 right-8 text-6xl text-blue-500">{{ emoji }}</div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: { type: String, default: 'Definición' },
  emoji: { type: String, default: '📝' }
});
</script>