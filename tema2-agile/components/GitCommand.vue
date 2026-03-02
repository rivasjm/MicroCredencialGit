<template>
  <div grid="~ cols-2 gap-8" m="t-8">
    <!-- Columna izquierda: ¿Para qué sirve? y ¿Cuándo se usa? -->
    <div>
      <InfoBox 
        icon="💡" 
        title="¿Para qué sirve?" 
        :content="purpose" 
        color="blue" 
        class="mb-6" 
      />
      
      <InfoBox 
        icon="⚡" 
        title="¿Cuándo se usa?" 
        :content="when" 
        color="green" 
      />
    </div>

    <!-- Columna derecha: Sintaxis y parámetros -->
    <div>
      <SyntaxBox 
        :command="command"
        :parameters="parameters"
      />
    </div>
  </div>
</template>

<script setup>
defineProps({
  purpose: String,
  when: String,
  command: String,
  parameters: Array
})
</script>