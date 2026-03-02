---
theme: default
background: https://cover.sli.dev
title: Tema 1 - Gestión Avanzada de la Configuración de Sistemas Software
mdc: true
layout: cover
---

## Tema 1
# Gestión Avanzada de la Configuración de Sistemas Software

<br>

#### Métodos de Desarrollo

<div class="absolute bottom-10">
  <span class="font-700">
    Juan M Rivas (rivasjm@unican.es)
  </span>
</div>

---

# Objetivos

<br>

<div grid="~ cols-2 md:cols-3 gap-4" class="mt-8">
  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🎯</span>
    <span class="font-bold text-green-800">Gestión de configuración de sistemas software</span>
  </div>
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🔄</span>
    <span class="font-bold text-blue-800">Integración y entrega continua</span>
  </div>
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">⚙️</span>
    <span class="font-bold text-yellow-800">DevOps</span>
  </div>
  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🗂️</span>
    <span class="font-bold text-purple-800">Gestionar versiones con Git</span>
  </div>
  <div class="bg-orange-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🏆</span>
    <span class="font-bold text-orange-800">Estrategias de la gestión de configuración más populares</span>
  </div>
  <div class="bg-pink-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🌱</span>
    <span class="font-bold text-pink-800">Estrategia Gitflow</span>
  </div>
</div>

---

# Bibliografía

<script setup>
import portadaSommerville from '/images/sommerville.jpg'
import portadaProGit from '/images/progit.png'
</script>

<br>

<ReferenciaBibliografica
  titulo="Software Engineering"
  autor="Ian Sommerville"
  edicion="10th Edition"
  editorial="Pearson"
  año="2016"
  isbn="978-0133943030"
  :portada="portadaSommerville"
/>

<br>

<ReferenciaBibliografica
  titulo="Pro Git"
  autor="Scott Chacon, Ben Straub"
  edicion="2nd Edition"
  editorial="Apress"
  año="2014"
  isbn="978-1484200773"
  enlace="https://git-scm.com/book/es/v2"
  :portada="portadaProGit"
/>

---

# Índice

<br>

1. Gestión de la configuración software
2. Control de versiones con Git  
3. Modelos organizativos con Git  

---
src: ./tema1.1-slides.md
---

---
src: ./tema1.2-slides.md
---

---
src: ./tema1.3-slides.md
---

---
src: ./tema1.4-slides.md
---