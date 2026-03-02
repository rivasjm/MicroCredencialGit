<!-- filepath: /Users/juan/Developer/teaching/MetodosDeDesarrollo/components/DefinicionDestacada.vue -->
<template>
  <div :class="[containerClass, mtClass, mbClass]">
    <span :class="titleClass">{{ title }}</span>
    <div class="p-4">
      <slot />
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
const props = defineProps({
  title: { type: String, required: true },
  color: { type: String, default: 'blue' },
  mt: { type: String, default: '0' }, // ejemplo: '4', '8'
  mb: { type: String, default: '0' }
})

const colorMap = {
  blue: {
    container: 'bg-blue-50 rounded-lg shadow-sm p-0',
    title: 'block w-full font-bold text-blue-700 text-lg bg-blue-200 py-2 rounded-t-lg text-left pl-4'
  },
  purple: {
    container: 'bg-purple-50 rounded-lg shadow-sm p-0',
    title: 'block w-full font-bold text-purple-700 text-lg bg-purple-200 py-2 rounded-t-lg text-left pl-4'
  },
  green: {
    container: 'bg-green-50 rounded-lg shadow-sm p-0',
    title: 'block w-full font-bold text-green-700 text-lg bg-green-200 py-2 rounded-t-lg text-left pl-4'
  },
  yellow: {
    container: 'bg-yellow-50 rounded-lg shadow-sm p-0',
    title: 'block w-full font-bold text-yellow-700 text-lg bg-yellow-200 py-2 rounded-t-lg text-left pl-4'
  },
  pink: {
    container: 'bg-pink-50 rounded-lg shadow-sm p-0',
    title: 'block w-full font-bold text-pink-700 text-lg bg-pink-200 py-2 rounded-t-lg text-left pl-4'
  },
  orange: {
    container: 'bg-orange-50 rounded-lg shadow-sm p-0',
    title: 'block w-full font-bold text-orange-700 text-lg bg-orange-200 py-2 rounded-t-lg text-left pl-4'
  }
}

const containerClass = computed(() => colorMap[props.color]?.container || colorMap.blue.container)
const titleClass = computed(() => colorMap[props.color]?.title || colorMap.blue.title)
const mtClass = computed(() => props.mt !== '0' ? `mt-${props.mt}` : '')
const mbClass = computed(() => props.mb !== '0' ? `mb-${props.mb}` : '')
</script>