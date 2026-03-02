<template>
  <div :class="boxClasses">
    <h3 :class="titleClasses">
      {{ icon }} {{ title }}
    </h3>
    <p :class="contentClasses" v-html="content"></p>
  </div>
</template>

<script setup>
const props = defineProps({
  icon: String,
  title: String,
  content: String,
  color: {
    type: String,
    default: 'blue'
  }
})

const colorMap = {
  blue: {
    box: 'bg-blue-50 border-blue-500 dark:bg-blue-900/30 dark:border-blue-400',
    title: 'text-blue-700 dark:text-blue-300',
    content: 'text-blue-800 dark:text-blue-200'
  },
  green: {
    box: 'bg-green-50 border-green-500 dark:bg-green-900/30 dark:border-green-400',
    title: 'text-green-700 dark:text-green-300',
    content: 'text-green-800 dark:text-green-200'
  },
  purple: {
    box: 'bg-purple-50 border-purple-500 dark:bg-purple-900/30 dark:border-purple-400',
    title: 'text-purple-700 dark:text-purple-300',
    content: 'text-purple-800 dark:text-purple-200'
  }
}

const boxClasses = `border-l-4 p-4 rounded-r-lg ${colorMap[props.color].box}`
const titleClasses = `font-bold text-lg mb-2 ${colorMap[props.color].title}`
const contentClasses = colorMap[props.color].content
</script>