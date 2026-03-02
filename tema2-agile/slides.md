---
theme: default
background: https://cover.sli.dev
title: Tema 2 - Metodologías de Desarrollo de Software Ágiles
mdc: true
layout: cover
---
 
## Tema 2
# Metodologías de Desarrollo de Software Ágiles

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

<div grid="~ cols-2 gap-6" class="mt-8">
  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🎯</span>
    <span class="font-bold text-green-800">Principios básicos de metodologías ágiles</span>
  </div>
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🔄</span>
    <span class="font-bold text-blue-800">Técnicas comunes en desarrollo ágil</span>
  </div>
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">⚙️</span>
    <span class="font-bold text-yellow-800">Principales metodologías ágiles y sus características</span>
  </div>
  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex items-center gap-2">
    <span class="text-2xl">🏆</span>
    <span class="font-bold text-purple-800">Desarrollar proyectos con Scrum</span>
  </div>
</div>

---

# Bibliografía

<div class="flex flex-col gap-4 mt-8">
  <ReferenciaBibliograficaSimple
    titulo="The Scrum Guide - The Definitive Guide to Scrum: The Rules of the Game"
    autor="Schwaber, K. and Sutherland, J."
  />
  <ReferenciaBibliograficaSimple
    titulo="User Stories Applied"
    autor="Cohn, M."
    año="2004"
    edicion="Addison-Wesley"
  />
  <!-- Nuevas referencias -->
  <ReferenciaBibliograficaSimple
    titulo="Lean Software Development: An Agile Toolkit"
    autor="Poppendieck, M. and Poppendieck, T."
    año="2003"
    edicion="Addison-Wesley"
  />
  <ReferenciaBibliograficaSimple
    titulo="Kanban: Successful Evolutionary Change for Your Technology Business"
    autor="Anderson, D. J. and Reinertsen, D. G."
    año="2010"
    edicion="Blue Hole Press"
  />
  <ReferenciaBibliograficaSimple
    titulo="Software Engineering"
    autor="Sommerville, I."
    año="2016"
    edicion="Addison Wesley, 10a edición"
  />
</div>

---

# Índice

1. **Concepto de Metodología Ágil**
2. **Lean**
3. **Scrum**
4. **Técnicas y Herramientas Ágiles**
5. **Otras Metodologías Ágiles**
6. **Sumario**

---

# Índice

1. <span style="color: red; font-weight: bold;">Concepto de Metodología Ágil</span>
    - Metodologías Ágiles y Metodologías No Ágiles
    - Manifiesto Ágil
    - Limitaciones de las Metodologías Ágiles
2. **Lean**
3. **Scrum**
4. **Técnicas y Herramientas Ágiles**
5. **Otras Metodologías Ágiles**
6. **Sumario**

---

# Metodologías Planificadas vs Ágiles

<DefinicionSimple title="Metodologías Fuertemente Planificadas" color="blue" mt="12">
  Se basan en la definición de un plan de trabajo al cual debemos de adherirnos y que es complejo o difícil de cambiar. Suele tener roles y procesos claramente definidos.
</DefinicionSimple>

<DefinicionSimple title="Metodologías Ágiles" color="purple" mt="12">
  Se basan en una organización del trabajo que permita la definición de planes de trabajo, procesos y productos fácilmente modificables en función de las <b>demandas de los usuarios</b>, con los cuales se debe mantener un permanente contacto y proporcionarles con frecuencia versiones parciales y operativas del software desarrollado.
</DefinicionSimple>

---

# Manifiesto Ágil : 4 Pilares

<br>
<br>
<br>

<div grid="~ cols-2 gap-4">
  <div class="bg-red-50 rounded-lg p-4 shadow-sm">
    <span class="text-2xl">🙋‍♂️</span>
    <span class="font-bold text-red-800"> Personas e interacciones personales</span>
    <br>
    <span>sobre procesos y herramientas.</span>
  </div>
  <div class="bg-green-50 rounded-lg p-4 shadow-sm">
    <span class="text-2xl">💻</span>
    <span class="font-bold text-green-800"> Software operativo</span>
    <br>
    <span>antes que extensos modelos software.</span>
  </div>
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm">
    <span class="text-2xl">🤝</span>
    <span class="font-bold text-blue-800"> Colaboración con el cliente</span>
    <br>
    <span>frente a renegociaciones de contrato.</span>
  </div>
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm">
    <span class="text-2xl">🔄</span>
    <span class="font-bold text-yellow-800"> Ser capaz de responder al cambio</span>
    <br>
    <span>antes que seguir un plan fijo.</span>
  </div>
</div>

<br>
<br>

[Ver el Manifiesto Ágil](https://agilemanifesto.org/)

---

# Manifiesto Ágil: 12 Principios (1-6)


<div grid="~ cols-2 gap-4" class="mt-8">

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">😊</span>
    <div>
      <span class="font-bold text-green-800">Satisfacción del cliente</span>
      <div class="text-sm mt-1">Entregas tempranas y continuas de software operativo.</div>
    </div>
  </div>

  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🔄</span>
    <div>
      <span class="font-bold text-yellow-800">Los cambios son bienvenidos</span>
      <div class="text-sm mt-1">Incluso en etapas avanzadas del desarrollo.</div>
    </div>
  </div>

  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🚀</span>
    <div>
      <span class="font-bold text-blue-800">Entregar software operativo frecuentemente</span>
      <div class="text-sm mt-1">Desde semanas hasta meses, preferiblemente en períodos cortos.</div>
    </div>
  </div>

  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🤝</span>
    <div>
      <span class="font-bold text-purple-800">Colaboración diaria</span>
      <div class="text-sm mt-1">Gestores y desarrolladores colaboran durante todo el proyecto.</div>
    </div>
  </div>

  <div class="bg-pink-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🌟</span>
    <div>
      <span class="font-bold text-pink-800">Individuos motivados</span>
      <div class="text-sm mt-1">Darles entorno, apoyo y confianza para realizar el trabajo.</div>
    </div>
  </div>

  <div class="bg-orange-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🗣️</span>
    <div>
      <span class="font-bold text-orange-800">Comunicación cara a cara</span>
      <div class="text-sm mt-1">La forma más eficiente y efectiva de comunicar información.</div>
    </div>
  </div>

</div>


[Fuente: https://agilemanifesto.org/principles.html](https://agilemanifesto.org/principles.html)


---

# Manifiesto Ágil: 12 Principios (7-12)

<div grid="~ cols-2 gap-4" class="mt-8">

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">📈</span>
    <div>
      <span class="font-bold text-green-800">Indicador de avance</span>
      <div class="text-sm mt-1">El principal indicador es la cantidad de software operativo entregado.</div>
    </div>
  </div>

  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🔋</span>
    <div>
      <span class="font-bold text-yellow-800">Desarrollo sostenible</span>
      <div class="text-sm mt-1">El desarrollo software debería ser sostenible.</div>
    </div>
  </div>

  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🏅</span>
    <div>
      <span class="font-bold text-blue-800">Excelencia técnica</span>
      <div class="text-sm mt-1">La excelencia técnica y los buenos diseños facilitan la agilidad.</div>
    </div>
  </div>

  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🧩</span>
    <div>
      <span class="font-bold text-purple-800">Simplicidad</span>
      <div class="text-sm mt-1">Maximizar el trabajo a no hacer es <a href="https://medium.com/@webseanhickey/the-evolution-of-a-software-engineer-db854689243" target="_blank">primordial</a>.</div>
    </div>
  </div>

  <div class="bg-pink-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🛠️</span>
    <div>
      <span class="font-bold text-pink-800">Equipos autoorganizados</span>
      <div class="text-sm mt-1">Las mejores arquitecturas y diseños emergen de equipos autoorganizados.</div>
    </div>
  </div>

  <div class="bg-orange-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🔍</span>
    <div>
      <span class="font-bold text-orange-800">Reflexión periódica</span>
      <div class="text-sm mt-1">El equipo debe reflexionar periódicamente sobre su eficiencia y productividad.</div>
    </div>
  </div>

</div>

[Fuente: https://agilemanifesto.org/principles.html](https://agilemanifesto.org/principles.html)

---
layout: statement
---

# ¿Qué problemas se os ocurre que puede tener la metodología ágil?

---

# ⚠️ Limitaciones de las Metodologías Ágiles

<div grid="~ cols-2 md:cols-3 gap-4" class="mt-16">

  <div class="bg-red-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🧑‍💼</span>
    <div>
      <span class="font-bold text-red-800">Involucrar al cliente</span>
      <div class="text-sm mt-1">Requiere participación activa y continua del cliente.</div>
    </div>
  </div>

  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🤝</span>
    <div>
      <span class="font-bold text-yellow-800">Actitud cooperativa</span>
      <div class="text-sm mt-1">Es imprescindible una personalidad colaborativa en el equipo.</div>
    </div>
  </div>

  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🛠️</span>
    <div>
      <span class="font-bold text-blue-800">Habilidades técnicas</span>
      <div class="text-sm mt-1">El equipo debe tener competencias técnicas adecuadas.</div>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">📋</span>
    <div>
      <span class="font-bold text-green-800">Identificación de prioridades</span>
      <div class="text-sm mt-1">Puede ser difícil definir prioridades e incrementos de software.</div>
    </div>
  </div>

  <div class="bg-pink-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🧹</span>
    <div>
      <span class="font-bold text-pink-800">Mantener la simplicidad</span>
      <div class="text-sm mt-1">Evitar el simple parcheo y mantener soluciones simples.</div>
    </div>
  </div>

  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">📑</span>
    <div>
      <span class="font-bold text-purple-800">Problemas contractuales</span>
      <div class="text-sm mt-1">Dificultades en la definición de contratos y alcance del proyecto.</div>
    </div>
  </div>

</div>

---

# Principales Tipos de Metodologías Ágiles

<div grid="~ cols-2 md:cols-4 gap-4" class="mt-16">

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">🏃‍♂️</span>
    <span class="font-bold text-green-800 mb-1">Scrum</span>
    <span class="text-sm text-green-700 text-center">Gestión de proyectos basada en sprints, roles definidos y reuniones periódicas.</span>
  </div>

  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">📋</span>
    <span class="font-bold text-blue-800 mb-1">Kanban</span>
    <span class="text-sm text-blue-700 text-center">Visualización del flujo de trabajo con tableros y gestión continua de tareas.</span>
  </div>

  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">💡</span>
    <span class="font-bold text-yellow-800 mb-1">Lean</span>
    <span class="text-sm text-yellow-700 text-center">Enfocado en la eficiencia, reducción de desperdicio y mejora continua.</span>
  </div>

  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">👨‍💻</span>
    <span class="font-bold text-purple-800 mb-1">EXtremeProgramming</span>
    <span class="text-sm text-purple-700 text-center">Prácticas técnicas como desarrollo iterativo, integración continua y programación en pareja.</span>
  </div>

</div>


<div class="bg-blue-50 border-l-4 border-blue-500 p-4 rounded shadow-lg max-w-2xl text-sm mt-12">
  <span class="font-bold text-blue-700">Según el <a href="https://stateofagile.com/" target="_blank">17th State of Agile Report</a>:</span>
  <ul class="list-disc ml-5 mt-2">
    <li>El <span class="font-bold text-green-700">71%</span> de las organizaciones usan metodologías ágiles.</li>
    <li>Dentro de Agile, el <span class="font-bold text-purple-700">63%</span> utilizan <b>Scrum</b> como marco principal.</li>
  </ul>
</div>

---

# Índice

1. **Concepto de Metodología Ágil**
2. <span style="color: red; font-weight: bold;">Lean</span>
3. **Scrum**
4. **Técnicas y Herramientas Ágiles**
5. **Otras Metodologías Ágiles**
6. **Sumario**

---

# Metodología <b>Lean</b>: Principios Fundamentales

<br>

<table class="w-full text-yellow-900 text-sm rounded overflow-hidden shadow-lg">
  <tbody>
    <tr class="bg-yellow-50">
      <td class="py-2 px-4 font-bold">Eliminar los desperdicios</td>
      <td class="py-2 px-4">Evitar tareas, procesos y recursos innecesarios.</td>
    </tr>
    <tr>
      <td class="py-2 px-4 font-bold">Fomentar el aprendizaje</td>
      <td class="py-2 px-4">Aprender de la experiencia y mejorar continuamente. Entender al cliente.</td>
    </tr>
    <tr class="bg-yellow-50">
      <td class="py-2 px-4 font-bold">Postergar las decisiones</td>
      <td class="py-2 px-4">Tomar decisiones importantes lo más tarde posible, con la mayor información disponible.</td>
    </tr>
    <tr>
      <td class="py-2 px-4 font-bold">Entregas rápidas</td>
      <td class="py-2 px-4">Realizar entregas tan rápido como sea posible para obtener feedback temprano.</td>
    </tr>
    <tr class="bg-yellow-50">
      <td class="py-2 px-4 font-bold">Delegar responsabilidades</td>
      <td class="py-2 px-4">El equipo debe tener autonomía y capacidad de decisión.</td>
    </tr>
    <tr>
      <td class="py-2 px-4 font-bold">Fomentar la integridad</td>
      <td class="py-2 px-4">Mantener la calidad y cohesión tanto del producto como del equipo.</td>
    </tr>
    <tr class="bg-yellow-50">
      <td class="py-2 px-4 font-bold">Visión global</td>
      <td class="py-2 px-4">Facilitar la comprensión del conjunto y el impacto de cada parte.</td>
    </tr>
  </tbody>
</table>

<br>

<div class="mt-8 text-sm text-yellow-900">
  <span class="font-bold">Referencia:</span> <i>Lean Software Development: An Agile Toolkit</i>, Mary & Tom Poppendieck, Addison-Wesley, 2003.
</div>

---

# Índice

1. **Concepto de Metodología Ágil**
2. **Lean**
3. <span style="color: red; font-weight: bold;">Scrum</span>
    - Roles en Scrum
    - Esquema de Scrum
    - Conceptos y Técnicas de Scrum
4. **Técnicas y Herramientas Ágiles**
5. **Otras Metodologías Ágiles**
6. **Sumario**

---

# Conceptos básicos de Scrum

<div grid="~ cols-2 gap-2" class="mt-8 max-w-4xl mx-auto">
  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex flex-col gap-2">
    <span class="text-2xl">📦</span>
    <span class="font-bold text-green-800">Marco de trabajo ágil</span>
    <span class="text-green-700 text-sm">Scrum es un marco para gestionar proyectos complejos, especialmente software.</span>
  </div>
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex flex-col gap-2">
    <span class="text-2xl">⏳</span>
    <span class="font-bold text-blue-800">Sprints</span>
    <span class="text-blue-700 text-sm">Ciclos cortos donde se entrega valor incrementalmente.</span>
  </div>
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex flex-col gap-2">
    <span class="text-2xl">👥</span>
    <span class="font-bold text-yellow-800">Roles definidos</span>
    <span class="text-yellow-700 text-sm">Scrum Team, Product Owner, Scrum Master.</span>
  </div>
  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex flex-col gap-2">
    <span class="text-2xl">📅</span>
    <span class="font-bold text-purple-800">Eventos clave definidos</span>
    <span class="text-purple-700 text-sm">Planificación del sprint, reuniones diarias y retrospectivas.</span>
  </div>
</div>

<!-- agil no significa que no haya ningún proceso establecido o una anarquía -->

---

# Roles en Scrum

<div class="flex justify-center items-center h-[28rem]">
  <div class="relative w-[38rem] h-[24rem]">
    <!-- Scrum Team - Arriba -->
    <div class="absolute top-0 left-1/2 transform -translate-x-1/2 w-80">
      <div class="bg-green-50 rounded-xl shadow-lg p-5 border border-green-200 flex flex-col items-start">
        <span class="font-bold text-green-800 text-base block mb-2 text-left w-full">
          👥 Scrum Team
        </span>
        <div class="text-green-700 text-xs mb-2 text-left w-full leading-snug">
          Equipo multidisciplinar que desarrolla el producto. Todos son iguales (Bus Factor).
        </div>
        <div class="text-green-700 text-xs text-left w-full leading-snug">
          Incluye todos los miembros necesarios para entregar incrementos de producto potencialmente entregables en cada sprint. 
        </div>
      </div>
    </div>
    <!-- Product Owner - Abajo más a la izquierda -->
    <div class="absolute bottom-4 left-[-3rem] w-80">
      <div class="bg-yellow-50 rounded-xl shadow-lg p-5 border border-yellow-200 flex flex-col items-start">
        <span class="font-bold text-yellow-800 text-base block mb-2 text-left w-full">
          🧑‍💼 Product Owner
        </span>
        <div class="text-yellow-700 text-xs mb-2 text-left w-full leading-snug">
          Define prioridades y requisitos, representa al cliente.
        </div>
        <div class="text-yellow-700 text-xs text-left w-full leading-snug">
          Su principal responsabilidad es maximizar el valor del producto resultante del trabajo del Equipo de Desarrollo, gestionando el backlog.
        </div>
      </div>
    </div>
    <!-- Scrum Master - Abajo más a la derecha -->
    <div class="absolute bottom-4 right-[-3rem] w-80">
      <div class="bg-blue-50 rounded-xl shadow-lg p-5 border border-blue-200 flex flex-col items-start">
        <span class="font-bold text-blue-800 text-base block mb-2 text-left w-full">
          🧑‍🏫 Scrum Master
        </span>
        <div class="text-blue-700 text-xs mb-2 text-left w-full leading-snug">
          Facilita el proceso, elimina impedimentos y fomenta la mejora continua.
        </div>
        <div class="text-blue-700 text-xs text-left w-full leading-snug">
          Ayuda a todos a comprender y adoptar la teoría, las prácticas, las reglas y los valores de Scrum.
        </div>
      </div>
    </div>
  </div>
</div>

---

# Proceso de desarrollo Scrum

<div class="flex justify-center mt-10">
  <img src="/images/scrum.svg" alt="Flujo Scrum" class="w-220 rounded" />
</div>

<div class="absolute bottom-6 left-6 text-blue-700 text-sm">
  <a href="https://github.com/isunican/docsProyectoIntegrado/wiki/actividadesScrum" target="_blank">https://github.com/isunican/docsProyectoIntegrado/wiki/actividadesScrum</a>
</div>

---

# Conceptos clave en Scrum

<div grid="~ cols-2 gap-4" class="mt-10">
  <div class="bg-green-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-green-800 text-lg mb-1 block">1️⃣ Velocidad del equipo</span>
    <span class="text-green-700 text-sm">Cantidad de trabajo (p.ej. puntos de historia) que el equipo puede completar en un sprint. Permite estimar la capacidad y planificar futuros sprints.</span>
  </div>
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-blue-800 text-lg mb-1 block">2️⃣ Definición de Completado</span>
    <span class="text-blue-700 text-sm">Criterios claros que debe cumplir una tarea para considerarse realmente terminada (ej: código revisado, probado, documentado y desplegado).</span>
    <div class="mt-2 text-xs">
      <a href="https://github.com/isunican/docsProyectoIntegrado/wiki/definicionCompletado" target="_blank" class="text-blue-600 underline">Definición de Completado en el Proyecto Integrado</a>
    </div>
  </div>
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-yellow-800 text-lg mb-1 block">3️⃣ Release Backlog</span>
    <span class="text-yellow-700 text-sm">Lista priorizada de funcionalidades y tareas que se espera entregar en una versión concreta del producto.</span>
  </div>
  <div class="bg-purple-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-purple-800 text-lg mb-1 block">4️⃣ Product Backlog Refinement</span>
    <span class="text-purple-700 text-sm">Proceso continuo de revisión, clarificación y priorización de los elementos del Product Backlog para asegurar que estén listos para ser abordados en futuros sprints.</span>
  </div>
</div>

---

# Sprint Burndown Chart

<div grid="~ cols-5 gap-12" class="items-center mt-8">
  <div class="col-span-2">
    <DefinicionCompacta title="Sprint Burndown Chart" emoji="📉">
      Gráfico que muestra el trabajo pendiente a lo largo del <b>sprint</b>.<br>
      Permiten visualizar el progreso y detectar desviaciones respecto a la planificación.
    </DefinicionCompacta>
  </div>
  
  <div class="col-span-3">
```mermaid {scale:0.7}
xychart-beta
  title "Sprint Burndown Chart"
    x-axis ["Día 1", "Día 2", "Día 3", "Día 4", "Día 5", "Día 8", "Día 9", "Día 10", "Día 11", "Día 12", "Día 13", "Día 14"]
    y-axis "Trabajo pendiente (h)" 0 --> 100
    line "Planificado" [100, 91, 82, 73, 64, 55, 46, 37, 28, 19, 10, 0]
    line "Real" [100, 92, 85, 75, 65, 45, 35, 25, 12, 5, 3, 0]
```
  </div>
</div>

---

# Índice

1. **Concepto de Metodología Ágil**
2. **Lean**
3. **Scrum**
4. <span style="color: red; font-weight: bold;">Técnicas y Herramientas Ágiles</span>
    - Historias de Usuario
    - Juego de la Planificación
    - Sprint y Spike
    - Desarrollo Basado en Pruebas
    - Programación por Pares
5. **Otras Metodologías Ágiles**
6. **Sumario**

---

# Historia de Usuario

<DefinicionSimple title="Historia de Usuario" color="yellow" class="mb-6">
  Una historia de usuario describe una funcionalidad del sistema que posee valor para algún stakeholder.<br>
  Es la unidad básica de trabajo en metodologías ágiles.
</DefinicionSimple>

<br>
<b>Compuesto de los siguientes 3 elementos:</b>

<div class="mt-4" grid="~ cols-3 gap-4">
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">🗂️</span>
    <span class="font-bold text-yellow-800 mb-1">Tarjeta</span>
    <span class="text-yellow-700 text-sm text-center">Cada historia se anota en una tarjeta física o digital, recordando que debe ser realizada.</span>
  </div>
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">💬</span>
    <span class="font-bold text-blue-800 mb-1">Conversación</span>
    <span class="text-blue-700 text-sm text-center">Diálogos entre usuarios, clientes, desarrolladores y testers para aclarar detalles y requisitos. Parte de estas conversaciones puede documentarse.</span>
  </div>
  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex flex-col items-center">
    <span class="text-3xl mb-2">✅</span>
    <span class="font-bold text-green-800 mb-1">Confirmación</span>
    <span class="text-green-700 text-sm text-center">Procedimiento para verificar que la historia se ha realizado correctamente (criterios de aceptación).</span>
  </div>
</div>

---

# Propiedades deseables de una Historia de Usuario

<div class="text-center mb-8">
  <span class="text-4xl">🎯</span>
  <h3 class="text-xl font-bold text-gray-700 mt-2">Una buena historia de usuario debe ser...</h3>
</div>

<div grid="~ cols-2 md:cols-3 gap-4" class="mt-8">
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🔄</span>
    <div>
      <span class="font-bold text-blue-800">Independiente</span>
      <div class="text-sm mt-1 text-blue-700">No debe depender de otras historias para poder desarrollarse e implementarse.</div>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">💬</span>
    <div>
      <span class="font-bold text-green-800">Negociable</span>
      <div class="text-sm mt-1 text-green-700">Los detalles pueden discutirse y modificarse.</div>
    </div>
  </div>

  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">⭐</span>
    <div>
      <span class="font-bold text-purple-800">Añade valor</span>
      <div class="text-sm mt-1 text-purple-700">Debe proporcionar valor real y tangible al usuario o stakeholder.</div>
    </div>
  </div>

  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">📏</span>
    <div>
      <span class="font-bold text-yellow-800">Estimable</span>
      <div class="text-sm mt-1 text-yellow-700">El equipo debe poder estimar el esfuerzo necesario para desarrollarla.</div>
    </div>
  </div>

  <div class="bg-pink-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">🧩</span>
    <div>
      <span class="font-bold text-pink-800">Pequeñas</span>
      <div class="text-sm mt-1 text-pink-700">Deben ser lo suficientemente pequeñas para completarse en un sprint.</div>
    </div>
  </div>

  <div class="bg-orange-50 rounded-lg p-4 shadow-sm flex gap-2 items-start">
    <span class="text-2xl">✅</span>
    <div>
      <span class="font-bold text-orange-800">Verificable</span>
      <div class="text-sm mt-1 text-orange-700">Debe ser posible comprobar que la funcionalidad cumple los criterios de aceptación.</div>
    </div>
  </div>
</div>

---

# Historia Épica (Epic)

<DefinicionSimple title="Historia Épica (Epic)" color="red" class="mt-12 mb-4">
  Una historia épica es una historia que por su <b>tamaño no puede ser desarrollada en un periodo corto de tiempo</b>, por lo que ha de ser <b>descompuesta en historias de usuario de menor tamaño</b>.
</DefinicionSimple>

<div grid="~ cols-3" class="items-center mt-12">
  <!-- Columna 1: historia épica -->
  <div class="flex flex-col items-center">
    <div class="bg-red-50 rounded-lg p-4 shadow-sm flex flex-col items-center w-40">
      <span class="text-3xl mb-2">📚</span>
      <span class="font-bold text-red-800 mb-1">Historia épica</span>
      <span class="text-red-700 text-xs text-center">Demasiado grande para un sprint</span>
    </div>
  </div>
  <!-- Columna 2: flecha -->
  <div class="flex justify-center items-center h-full">
    <span class="text-3xl">➡️</span>
  </div>
  <!-- Columna 3: historias de usuario -->
  <div grid="~ cols-2 gap-2" class="w-full max-w-xs">
    <div class="bg-green-50 rounded-lg p-2 shadow-sm flex flex-col items-center">
      <span class="text-lg mb-1">📝</span>
      <span class="font-bold text-green-800 text-xs mb-1">Historia 1</span>
      <span class="text-green-700 text-xs text-center">Sprint-sized</span>
    </div>
    <div class="bg-green-50 rounded-lg p-2 shadow-sm flex flex-col items-center">
      <span class="text-lg mb-1">📝</span>
      <span class="font-bold text-green-800 text-xs mb-1">Historia 2</span>
      <span class="text-green-700 text-xs text-center">Sprint-sized</span>
    </div>
    <div class="bg-green-50 rounded-lg p-2 shadow-sm flex flex-col items-center">
      <span class="text-lg mb-1">📝</span>
      <span class="font-bold text-green-800 text-xs mb-1">Historia 3</span>
      <span class="text-green-700 text-xs text-center">Sprint-sized</span>
    </div>
    <div class="bg-green-50 rounded-lg p-2 shadow-sm flex flex-col items-center">
      <span class="text-lg mb-1">📝</span>
      <span class="font-bold text-green-800 text-xs mb-1">Historia 4</span>
      <span class="text-green-700 text-xs text-center">Sprint-sized</span>
    </div>
  </div>
</div>

---

# Precisión y Esfuerzo en las Estimaciones

<div class="flex justify-center mt-8 mb-8">
  <img src="/images/precision-estimacion.png" alt="Precisión en la estimación ágil" class="rounded shadow-lg max-w-xl w-full" />
</div>

---

# Principios de la Estimación Ágil

<div grid="~ cols-1 gap-6" class="mt-8 max-w-4xl mx-auto">
  <div class="bg-blue-50 rounded-lg p-6 shadow-sm flex gap-4 items-start">
    <span class="text-3xl">🤝</span>
    <div>
      <span class="font-bold text-blue-800 text-lg mb-2 block">1️⃣ Estimaciones compartidas y consensuadas</span>
      <span class="text-blue-700 text-sm">Las estimaciones deben ser realizadas por todo el equipo de desarrollo, no por una sola persona. El consenso mejora la precisión y aumenta el compromiso del equipo.</span>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-6 shadow-sm flex gap-4 items-start">
    <span class="text-3xl">🔢</span>
    <div>
      <span class="font-bold text-green-800 text-lg mb-2 block">2️⃣ Escala discreta (Fibonacci Modificada)</span>
      <span class="text-green-700 text-sm">Utilizar valores de la secuencia de Fibonacci modificada (0, 0.5, 1, 2, 3, 5, 8, 13, 20, 40, 100) para evitar falsas precisiones</span>
      <div class="mt-3 flex gap-2 flex-wrap">
        <span class="bg-green-200 px-2 py-1 rounded text-xs">0</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">0.5</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">1</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">2</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">3</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">5</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">8</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">13</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">20</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">40</span>
        <span class="bg-green-200 px-2 py-1 rounded text-xs">100</span>
      </div>
    </div>
  </div>
</div>

---

# 🃏 Planning Poker: El Proceso (1-4)

<div class="text-center mb-6 mt-12">
  <h3 class="text-xl font-bold text-gray-700 mt-2">Técnica colaborativa para estimación</h3>
</div>

<div grid="~ cols-2 gap-4" class="mt-6">
  <div class="bg-yellow-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">1️⃣</span>
    <div>
      <span class="font-bold text-yellow-800">Reunir al equipo</span><br>
      <span class="text-yellow-700 text-sm">Se reúne al equipo de desarrollo completo.</span>
    </div>
  </div>

  <div class="bg-blue-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">2️⃣</span>
    <div>
      <span class="font-bold text-blue-800">Distribir cartas</span><br>
      <span class="text-blue-700 text-sm">Cada miembro recibe cartas con los valores de la escala de estimación (fibonacci).</span>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">3️⃣</span>
    <div>
      <span class="font-bold text-green-800">Presentar elemento</span><br>
      <span class="text-green-700 text-sm">El moderador presenta el elemento a estimar.</span>
    </div>
  </div>

  <div class="bg-purple-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">4️⃣</span>
    <div>
      <span class="font-bold text-purple-800">Aclarar dudas</span><br>
      <span class="text-purple-700 text-sm">Los miembros piden aclaraciones si es necesario.</span>
    </div>
  </div>
</div>

---

# 🃏 Planning Poker: El Proceso (5-8)

<div grid="~ cols-2 gap-4" class="mt-8">
  <div class="bg-pink-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">5️⃣</span>
    <div>
      <span class="font-bold text-pink-800">Estimación privada</span><br>
      <span class="text-pink-700 text-sm">Cada miembro escoge una carta con su estimación, manteniéndola oculta.</span>
    </div>
  </div>

  <div class="bg-orange-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">6️⃣</span>
    <div>
      <span class="font-bold text-orange-800">Revelar cartas</span><br>
      <span class="text-orange-700 text-sm">Cuando todos han estimado, se muestran las cartas simultáneamente.</span>
    </div>
  </div>

  <div class="bg-red-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">7️⃣</span>
    <div>
      <span class="font-bold text-red-800">Discutir diferencias</span><br>
      <span class="text-red-700 text-sm">Si hay variaciones significativas, se discuten brevemente y se vuelve al paso 5.</span>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-4 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">8️⃣</span>
    <div>
      <span class="font-bold text-green-800">Consenso final</span><br>
      <span class="text-green-700 text-sm">Si no hay diferencias significativas, se selecciona el valor consensuado.</span>
    </div>
  </div>
</div>

<div class="mt-8 bg-blue-50 border-l-4 border-blue-500 p-4 rounded shadow-lg max-w-2xl mx-auto text-sm">
  <span class="font-bold text-blue-700">🎯 Objetivo:</span><br>
  <span class="text-blue-800">Obtener estimaciones más precisas aprovechando la sabiduría colectiva del equipo y evitando el sesgo de anclaje.</span>
</div>

---

# Ejemplo Visual: Planning Poker en Acción

<div class="text-center mb-6">
  <span class="text-4xl">🎲🃏</span>
  <h3 class="text-xl font-bold text-gray-700 mt-12">Historia: "Yo como usuario quiero poder ordenar las películas por su fecha de estreno"</h3>
</div>

<div grid="~ cols-2 gap-8" class="mb-8">
  <!-- Primera ronda -->
  <div class="bg-gray-100 rounded-lg p-4 shadow-sm">
    <div class="text-center mb-4">
      <span class="font-bold text-gray-800">Primera ronda - Cartas reveladas:</span>
    </div>
    <div class="flex gap-4 justify-center">
      <div class="bg-white border-2 border-red-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">Ana</div>
        <div class="text-2xl font-bold text-red-600">3</div>
      </div>
      <div class="bg-white border-2 border-yellow-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">Carlos</div>
        <div class="text-2xl font-bold text-yellow-600">8</div>
      </div>
      <div class="bg-white border-2 border-blue-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">María</div>
        <div class="text-2xl font-bold text-blue-600">5</div>
      </div>
      <div class="bg-white border-2 border-green-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">Jorge</div>
        <div class="text-2xl font-bold text-green-600">5</div>
      </div>
    </div>
    <div class="text-center mt-4">
      <span class="text-sm text-red-600">⚠️ Diferencias significativas → Discusión</span>
    </div>
  </div>
  <!-- Segunda ronda -->
  <div class="bg-green-100 rounded-lg p-4 shadow-sm">
    <div class="text-center mb-4">
      <span class="font-bold text-green-800">Segunda ronda - Después de la discusión:</span>
    </div>
    <div class="flex gap-4 justify-center">
      <div class="bg-white border-2 border-green-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">Ana</div>
        <div class="text-2xl font-bold text-green-600">5</div>
      </div>
      <div class="bg-white border-2 border-green-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">Carlos</div>
        <div class="text-2xl font-bold text-green-600">5</div>
      </div>
      <div class="bg-white border-2 border-green-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">María</div>
        <div class="text-2xl font-bold text-green-600">5</div>
      </div>
      <div class="bg-white border-2 border-blue-300 rounded p-2 text-center">
        <div class="text-sm text-gray-600">Jorge</div>
        <div class="text-2xl font-bold text-blue-600">3</div>
      </div>
    </div>
    <div class="text-center mt-4">
      <span class="text-lg font-bold text-green-600">✅ Consenso: 5 puntos de historia</span>
    </div>
  </div>
</div>

---

# Sprint y Spike

<div grid="~ cols-2 gap-6" class="mt-4">
  <div>
    <Definicion title="Sprint" emoji="🏃‍♂️">
      Un <b>sprint</b> es una iteración de duración concreta y corta, al final de la cual se produce software potencialmente entregable.
    </Definicion>
    <div class="mt-4 bg-green-50 border-l-4 border-green-500 p-4 rounded shadow-lg text-sm">
      <span class="font-bold text-green-700">⏳ Duración típica:</span> 1 a 4 semanas<br>
      <span class="font-bold text-green-700">🎯 Objetivo:</span> Entregar valor al usuario de forma incremental y frecuente.
    </div>
  </div>
  <div>
    <Definicion title="Spike" emoji="🧪">
      Un <b>spike</b> es una iteración en la que no se libera nuevo código instalable o probado por usuarios. Se utiliza para experimentar, investigar, aprender nuevas tecnologías, probar algoritmos, generar documentación o productos de marketing.
    </Definicion>
    <div class="mt-4 bg-yellow-50 border-l-4 border-yellow-500 p-4 rounded shadow-lg text-sm">
      <span class="font-bold text-yellow-700">🔍 Usos:</span> Investigación técnica, prototipos, formación, documentación, marketing.
    </div>
  </div>
</div>

---

# Desarrollo Dirigido por Pruebas (TDD)

<DefinicionSimple title="Test-Driven Development" color="blue" class="mt-12 mb-6">
  Es una práctica de desarrollo de software que invierte el proceso tradicional: primero se escriben las pruebas automatizadas y luego el código que las satisface.
</DefinicionSimple>

<div class="flex justify-center mt-16">

```mermaid {scale:0.43}
flowchart LR
    A[📝 Escribir test que falle] --> B{🔴 Ejecutar tests<br/>El nuevo test debe fallar}
    B --> C[💻 Escribir código mínimo<br/>que haga pasar el test]
    C --> D{🟢 Ejecutar todos los tests<br/>¿Pasan todos?}
    D -->|No| E[🔧 Arreglar código<br/>con cambios mínimos]
    E --> D
    D -->|Sí| F[🔄 Refactorizar código<br/>manteniendo tests pasando]
    F --> G{🎯 ¿Necesitas más<br/>funcionalidad?}
    G -->|Sí| A
    G -->|No| H[✅ Completado]
    
    style A fill:#fef2f2,stroke:#dc2626
    style B fill:#fef2f2,stroke:#dc2626
    style C fill:#f0fdf4,stroke:#16a34a
    style D fill:#f0fdf4,stroke:#16a34a
    style F fill:#fefce8,stroke:#ca8a04
    style H fill:#eff6ff,stroke:#2563eb
```
</div>

---

# Programación por Pares

<DefinicionSimple title="Programación por Pares" emoji="👥">
  Se codifica por parejas, donde una persona escribe el código y la otra persona supervisa y aporta ideas. Los roles se permutan con frecuencia.
</DefinicionSimple>

<div grid="~ cols-2 gap-4" class="mt-12">
  <!-- Imagen conceptual -->
  <div class="bg-gray-50 rounded-lg p-6 shadow-sm flex flex-col items-center justify-center">
    <div class="text-6xl mb-4">👨‍💻👩‍💻</div>
    <div class="text-center">
      <span class="font-bold text-gray-800">Driver + Navigator</span><br>
      <span class="text-gray-600 text-sm">Roles intercambiables</span>
    </div>
  </div>
  
  <!-- Beneficios -->
  <div class="space-y-1">
    <div class="bg-red-50 rounded p-1 shadow-sm flex gap-1 items-start">
      <span class="text-base">🐛</span>
      <div>
        <span class="font-bold text-red-800 text-xs">Menos errores en el código.</span><br>
      </div>
    </div>
    <div class="bg-blue-50 rounded p-1 shadow-sm flex gap-1 items-start">
      <span class="text-base">📦</span>
      <div>
        <span class="font-bold text-blue-800 text-xs">Código más conciso y eficiente.</span><br>
      </div>
    </div>
    <div class="bg-green-50 rounded p-1 shadow-sm flex gap-1 items-start">
      <span class="text-base">🔄</span>
      <div>
        <span class="font-bold text-green-800 text-xs">Se detectan más refactorizaciones posibles.</span><br>
      </div>
    </div>
    <div class="bg-purple-50 rounded p-1 shadow-sm flex gap-1 items-start">
      <span class="text-base">🔍</span>
      <div>
        <span class="font-bold text-purple-800 text-xs">Revisión continua. El observador revisa el código.</span><br>
      </div>
    </div>
    <div class="bg-yellow-50 rounded p-1 shadow-sm flex gap-1 items-start">
      <span class="text-base">🤝</span>
      <div>
        <span class="font-bold text-yellow-800 text-xs">El código no pertenece a una sola persona.</span><br>
      </div>
    </div>
  </div>
</div>

---

# Índice

1. **Concepto de Metodología Ágil**
2. **Lean**
3. **Scrum**
4. **Técnicas y Herramientas Ágiles**
5. <span style="color: red; font-weight: bold;">Otras Metodologías Ágiles</span>
    - Kanban
    - Extreme Programming (XP)
6. **Sumario**

---

# Metodología Kanban

<DefinicionSimple title="Kanban" emoji="📋">
  Sistema visual de gestión del flujo de trabajo que busca encontrar un ritmo de trabajo sostenible y óptimo mediante la limitación del trabajo en progreso.
</DefinicionSimple>

<div grid="~ cols-2 gap-6" class="mt-8">
  <div class="bg-blue-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-blue-800 text-lg mb-2 block">🎯 Objetivo Principal</span>
    <span class="text-blue-700 text-sm">Encontrar un ritmo de trabajo sostenible y óptimo.</span>
  </div>
  
  <div class="bg-purple-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-purple-800 text-lg mb-2 block">🔗 Base Teórica</span>
    <span class="text-purple-700 text-sm">Aplica la Teoría de las Restricciones para optimizar el flujo.</span>
  </div>
  
  <div class="bg-red-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-red-800 text-lg mb-2 block">🚧 Identificación</span>
    <span class="text-red-700 text-sm">Busca identificar y eliminar cuellos de botella en los procesos.</span>
  </div>
  
  <div class="bg-green-50 rounded-lg p-4 shadow-sm">
    <span class="font-bold text-green-800 text-lg mb-2 block">👁️ Visualización</span>
    <span class="text-green-700 text-sm">Para identificar cuellos de botella, debemos visualizar el proceso.</span>
  </div>
</div>

---

# Filosofía Kanban

Gestión basada en recursos y capacidades

<div grid="~ cols-2 gap-4" class="mt-8 max-w-4xl mx-auto">
  <div class="bg-yellow-50 rounded-lg p-6 shadow-sm flex gap-4 items-start">
    <span class="text-3xl">👥</span>
    <div>
      <span class="font-bold text-yellow-800 text-lg mb-2 block">1️⃣ Recursos del equipo</span>
      <span class="text-yellow-700 text-sm">El equipo dispone de recursos para realizar el trabajo.</span>
    </div>
  </div>

  <div class="bg-blue-50 rounded-lg p-6 shadow-sm flex gap-4 items-start">
    <span class="text-3xl">⚡</span>
    <div>
      <span class="font-bold text-blue-800 text-lg mb-2 block">2️⃣ Capacidad determinada</span>
      <span class="text-blue-700 text-sm">Cada recurso tiene una capacidad limitada.</span>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-6 shadow-sm flex gap-4 items-start">
    <span class="text-3xl">🎫</span>
    <div>
      <span class="font-bold text-green-800 text-lg mb-2 block">3️⃣ Señalización de capacidad</span>
      <span class="text-green-700 text-sm">Si hay capacidad libre, se libera una tarjeta para admitir más trabajo.</span>
    </div>
  </div>

  <div class="bg-red-50 rounded-lg p-6 shadow-sm flex gap-4 items-start">
    <span class="text-3xl">🚫</span>
    <div>
      <span class="font-bold text-red-800 text-lg mb-2 block">4️⃣ Control de saturación</span>
      <span class="text-red-700 text-sm">Sin capacidad libre, no se pueden solicitar más tareas.</span>
    </div>
  </div>
</div>

---

# 🎫 Método Kanban: Implementación práctica

<div grid="~ cols-2 gap-4" class="mt-12">
  <div class="bg-purple-50 rounded-lg p-6 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">1️⃣</span>
    <div>
      <span class="font-bold text-purple-800 text-lg mb-2 block">Tarjetas de tareas</span>
      <span class="text-purple-700 text-sm">Las tareas a realizar se escriben en tarjetas que representan unidades de trabajo.</span>
    </div>
  </div>

  <div class="bg-blue-50 rounded-lg p-6 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">2️⃣</span>
    <div>
      <span class="font-bold text-blue-800 text-lg mb-2 block">Capacidad por recurso</span>
      <span class="text-blue-700 text-sm">Cada miembro del equipo puede admitir un número determinado de tarjetas simultáneas.</span>
    </div>
  </div>

  <div class="bg-red-50 rounded-lg p-6 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">3️⃣</span>
    <div>
      <span class="font-bold text-red-800 text-lg mb-2 block">WIP limitado</span>
      <span class="text-red-700 text-sm">La cantidad de trabajo en progreso (Work In Progress) es limitada.</span>
    </div>
  </div>

  <div class="bg-green-50 rounded-lg p-6 shadow-sm flex gap-3 items-start">
    <span class="text-2xl">4️⃣</span>
    <div>
      <span class="font-bold text-green-800 text-lg mb-2 block">Señalización de disponibilidad</span>
      <span class="text-green-700 text-sm">Cuando un recurso puede admitir más trabajo, debe señalarse para asignación.</span>
    </div>
  </div>
</div>

---

# Ejemplo de Tablero Kanban

<div grid="~ cols-4 gap-3" class="mt-24 text-sm">
  <!-- Columna To Do -->
  <div class="bg-red-50 rounded-lg p-3 shadow-sm">
    <div class="font-bold text-red-800 text-center mb-3 text-base">📝 To Do</div>
    <div class="space-y-2">
      <div class="bg-white p-2 rounded border border-red-200">
        <div class="text-xs text-gray-600">Tarea #1</div>
        <div class="text-red-700 font-medium text-xs">Login usuario</div>
      </div>
      <div class="bg-white p-2 rounded border border-red-200">
        <div class="text-xs text-gray-600">Tarea #2</div>
        <div class="text-red-700 font-medium text-xs">Base de datos</div>
      </div>
      <div class="bg-white p-2 rounded border border-red-200">
        <div class="text-xs text-gray-600">Tarea #3</div>
        <div class="text-red-700 font-medium text-xs">API REST</div>
      </div>
    </div>
  </div>

  <!-- Columna In Progress -->
  <div class="bg-yellow-50 rounded-lg p-3 shadow-sm">
    <div class="font-bold text-yellow-800 text-center mb-3 text-base">⚙️ In Progress</div>
    <div class="space-y-2">
      <div class="bg-white p-2 rounded border border-yellow-200">
        <div class="text-xs text-gray-600">Tarea #4</div>
        <div class="text-yellow-700 font-medium text-xs">Dashboard</div>
        <div class="text-xs text-gray-500">👤 Ana</div>
      </div>
      <div class="bg-white p-2 rounded border border-yellow-200">
        <div class="text-xs text-gray-600">Tarea #5</div>
        <div class="text-yellow-700 font-medium text-xs">Tests unitarios</div>
        <div class="text-xs text-gray-500">👤 Carlos</div>
      </div>
    </div>
  </div>

  <!-- Columna Review -->
  <div class="bg-blue-50 rounded-lg p-3 shadow-sm">
    <div class="font-bold text-blue-800 text-center mb-3 text-base">👀 Review <span class="text-xs">(1/2)</span></div>
    <div class="space-y-2">
      <div class="bg-white p-2 rounded border border-blue-200">
        <div class="text-xs text-gray-600">Tarea #6</div>
        <div class="text-blue-700 font-medium text-xs">Autenticación</div>
        <div class="text-xs text-gray-500">👤 María</div>
      </div>
    </div>
  </div>

  <!-- Columna Done -->
  <div class="bg-green-50 rounded-lg p-3 shadow-sm">
    <div class="font-bold text-green-800 text-center mb-3 text-base">✅ Done</div>
    <div class="space-y-2">
      <div class="bg-white p-2 rounded border border-green-200">
        <div class="text-xs text-gray-600">Tarea #7</div>
        <div class="text-green-700 font-medium text-xs">Configuración</div>
      </div>
      <div class="bg-white p-2 rounded border border-green-200">
        <div class="text-xs text-gray-600">Tarea #8</div>
        <div class="text-green-700 font-medium text-xs">Documentación</div>
      </div>
    </div>
  </div>
</div>

---

# Tablero Kanban físico

<div class="flex justify-center items-center mt-8">
  <img src="/images/kanban1.jpeg" alt="Ejemplo de tablero Kanban físico" class="rounded shadow-lg max-w-xl w-full" />
</div>

---

# Tablero Kanban físico

<div class="flex justify-center items-center mt-6">
  <img src="/images/kanban4.png" alt="Ejemplo de tablero Kanban físico" class="rounded shadow-lg max-w-xl w-full" />
</div>

---

# Tablero Kanban virtual (Jira)

<div class="flex justify-center items-center mt-8">
  <img src="/images/kanban2.png" alt="Ejemplo de tablero Kanban virtual" class="rounded shadow-lg max-w-xl w-full" />
</div>

<div class="flex justify-end items-start mt-2 mb-[-2rem]">
  <img src="/images/Jira_Logo.svg.png" alt="Jira Logo" class="w-32 h-auto mr-2" />
</div>

---

# Tablero Kanban virtual (Scrumdesk)

<div class="flex justify-center items-center mt-8">
  <img src="/images/kanban3.png" alt="Ejemplo de tablero Kanban virtual" class="rounded shadow-lg max-w-2xl w-full" />
</div>

<div class="flex justify-end items-start mt-6 mb-[-2rem]">
  <img src="/images/scrumdesk.png" alt="Scrumdesk Logo" class="w-32 h-auto mr-2" />
</div>

---

# Propiedades Fundamentales de Kanban

<div class="mt-12 max-w-3xl mx-auto">
  <ol class="space-y-2 text-lg">
    <li class="flex items-start gap-3">
      <span class="font-bold text-blue-600 mt-1">1.</span>
      <div>
        <span class="font-semibold">Limitar el Work In Progress</span>
        <div class="text-sm text-gray-600 mt-1">Establecer límites claros en la cantidad de trabajo simultáneo.</div>
      </div>
    </li>
    <li class="flex items-start gap-3">
      <span class="font-bold text-blue-600 mt-1">2.</span>
      <div>
        <span class="font-semibold">Visualizar el flujo de trabajo</span>
        <div class="text-sm text-gray-600 mt-1">Hacer visible todo el proceso mediante tableros Kanban.</div>
      </div>
    </li>
    <li class="flex items-start gap-3">
      <span class="font-bold text-blue-600 mt-1">3.</span>
      <div>
        <span class="font-semibold">Medir y optimizar</span>
        <div class="text-sm text-gray-600 mt-1">Recoger métricas para mejorar continuamente el flujo.</div>
      </div>
    </li>
    <li class="flex items-start gap-3">
      <span class="font-bold text-blue-600 mt-1">4.</span>
      <div>
        <span class="font-semibold">Reglas explícitas</span>
        <div class="text-sm text-gray-600 mt-1">Definir y comunicar claramente las reglas de trabajo.</div>
      </div>
    </li>
    <li class="flex items-start gap-3">
      <span class="font-bold text-blue-600 mt-1">5.</span>
      <div>
        <span class="font-semibold">Gestión basada en métricas</span>
        <div class="text-sm text-gray-600 mt-1">Usar datos cuantitativos para tomar decisiones de mejora.</div>
      </div>
    </li>
  </ol>
</div>

---

# Extreme Programming (XP)

<DefinicionSimple title="Extreme Programming (XP)" emoji="👨‍💻">
  XP es una metodología ágil basada en prácticas concretas y disciplinadas para lograr excelencia técnica y satisfacción del cliente mediante colaboración intensa, ciclos de feedback rápidos y mejora continua.
</DefinicionSimple>

<div grid="~ cols-2 gap-2" m="t-5">
  <div>
    <div class="font-bold text-blue-800 mb-2 text-lg">📊 Planificación y Gestión</div>
    <ul class="list-disc ml-5 text-blue-700 text-sm space-y-1">
      <li><b>Historias de Usuario:</b> Requisitos escritos como descripciones breves y priorizables.</li>
      <li><b>Juego de la Planificación:</b> Cliente y desarrolladores deciden qué historias abordar en cada iteración.</li>
      <li><b>Entregas Pequeñas:</b> Software funcional entregado en ciclos cortos (1-3 semanas).</li>
      <li><b>Ritmo Sostenible:</b> Se evita el sobreesfuerzo, buscando productividad y calidad a largo plazo.</li>
    </ul>
  </div>
  <div>
    <div class="font-bold text-purple-800 mb-2 text-lg">🎨 Diseño</div>
    <ul class="list-disc ml-5 text-purple-700 text-sm space-y-1">
      <li><b>Diseño Simple:</b> El diseño más sencillo posible para los requisitos actuales.</li>
      <li><b>Refactorización:</b> Mejorar la estructura interna del código sin cambiar su comportamiento.</li>
    </ul>
  </div>
</div>

---

# Extreme Programming (XP) (cont.)

<DefinicionSimple title="Extreme Programming (XP)" emoji="👨‍💻">
  XP es una metodología ágil basada en prácticas concretas y disciplinadas para lograr excelencia técnica y satisfacción del cliente mediante colaboración intensa, ciclos de feedback rápidos y mejora continua.
</DefinicionSimple>

<div grid="~ cols-2 gap-2" m="t-5">
  <div>
    <div class="font-bold text-green-800 mb-2 text-lg">💻 Codificación</div>
    <ul class="list-disc ml-5 text-green-700 text-sm space-y-1">
      <li><b>Programación en Parejas:</b> Dos programadores trabajan juntos, alternando roles.</li>
      <li><b>Propiedad Colectiva del Código:</b> Todos pueden mejorar cualquier parte del código.</li>
      <li><b>Integración Continua:</b> Cambios integrados y probados varias veces al día.</li>
      <li><b>Estándares de Codificación:</b> Reglas comunes para escribir código legible y uniforme.</li>
    </ul>
  </div>
  <div>
    <div class="font-bold text-yellow-800 mb-2 text-lg">✅ Pruebas</div>
    <ul class="list-disc ml-5 text-yellow-700 text-sm space-y-1">
      <li><b>TDD (Test-Driven Development):</b> Escribir primero la prueba, luego el código, y refactorizar.</li>
      <li><b>Pruebas de Aceptación:</b> El cliente define pruebas automatizadas para validar historias completadas.</li>
    </ul>
  </div>
</div>

---

# Índice

1. **Concepto de Metodología Ágil**
2. **Lean**
3. **Scrum**
4. **Técnicas y Herramientas Ágiles**
5. **Otras Metodologías Ágiles**
6. <span style="color: red; font-weight: bold;">Sumario</span>

---

# 📝 ¿Qué Tengo que Saber de Todo Esto?


<div class="bg-blue-50 border-l-4 mt-10 border-blue-500 p-4 rounded shadow-lg max-w-2xl mx-auto text-base space-y-3">
  <ul class="list-disc ml-5">
    <p>✅ Comprender los principios del manifiesto ágil.</p>
    <p>✅ Comprender los principios de las metodologías Lean.</p>
    <p>✅ Saber discernir cuando una metodología cumple con los principios del manifiesto ágil o de la filosofía Lean.</p>
    <p>✅ Conocer la terminología y las técnicas asociadas a la metodología Scrum.</p>
    <p>✅ Ser capaz de trabajar como miembro de un Scrum Team.</p>
    <p>✅ Ser capaz de utilizar una herramienta de gestión de proyectos Scrum.</p>
    <p>✅ Comprender los principios y objetivos de la metodología Kanban.</p>
    <p>✅ Comprender los principios y organización de la metodología XP.</p>
  </ul>
</div>

---


## Silicon Valley S01E05 scrum scene

<div class="w-full h-full flex items-center justify-center">
  <Youtube id="oyVksFviJVE" class="w-full h-[50vh] max-h-[30vh]" />
</div>
