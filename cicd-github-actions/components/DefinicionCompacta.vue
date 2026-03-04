<template>
  <div class="relative bg-gradient-to-r from-blue-50 to-indigo-50 border-l-2 border-blue-400 p-3 rounded shadow-md max-w-sm mx-auto my-3 hover:shadow-lg transition-shadow duration-200">
    
    <!-- Header with emoji and title -->
    <div class="flex items-center gap-2 mb-2">
      <span v-if="emoji" class="text-lg">{{ emoji }}</span>
      <span class="font-semibold text-sm text-blue-800">
        {{ title }}
      </span>
    </div>
    
    <!-- Content -->
    <div class="text-gray-600 text-sm leading-snug">
      <slot />
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: { type: String, default: 'Definición' },
  emoji: { type: String, default: '📝' }
});
</script>