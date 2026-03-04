---
theme: default
background: https://cover.sli.dev
title: CI/CD con GitHub Actions
info: |
  ## Microcredencial: Git
  ### CI/CD con github Actions
drawings:
  persist: false
mdc: true

---

  ## Microcredencial Git
  # CI/CD con Github Actions

---

# Índice 

<br>

1. Introducción teórica
2. GitHub Actions

---

# Dev vs Ops

<div grid="~ cols-2 gap-2" m="t-10">
  <div>
    <h3 class="text-blue-600">👨‍💻 Desarrollo (Dev)</h3>
    <ul>
      <li><b>Objetivo:</b> Crear nuevas funcionalidades</li>
      <li><b>Mentalidad:</b> "Cambio y velocidad"</li>
      <li><b>Métricas:</b> Velocidad de desarrollo, nuevas features</li>
      <li><b>Responsabilidad:</b> Hasta el deployment</li>
    </ul>
    <div class="mt-4 p-3 bg-blue-100 rounded">
      <p class="text-sm">"Funciona en mi máquina" 🤷‍♂️</p>
    </div>
  </div>
  
  <div>
    <h3 class="text-red-600">🔧 Operaciones (Ops)</h3>
    <ul>
      <li><b>Objetivo:</b> Mantener sistemas estables y seguros</li>
      <li><b>Mentalidad:</b> "Estabilidad y control"</li>
      <li><b>Métricas:</b> Uptime, rendimiento, seguridad</li>
      <li><b>Responsabilidad:</b> Producción y mantenimiento</li>
    </ul>
    <div class="mt-4 p-3 bg-red-100 rounded">
      <p class="text-sm">"No toques nada que funcione" 🚫</p>
    </div>
  </div>
</div>

<div class="mt-6 text-center">
  <div class="text-4xl mb-2">⚔️</div>
  <p class="text-lg font-semibold text-gray-600">Conflicto natural entre velocidad y estabilidad</p>
</div>

<!-- operaciones quiere que el servidor funcione y no lo toques -->

---

# DevOps

<Definicion title="DevOps" emoji="🔄">
  DevOps es un conjunto de prácticas, técnicas y herramientas que unifica los equipos de desarrollo de software (Dev) y operaciones (Ops).
</Definicion>

<div grid="~ cols-2 gap-2" m="t-5">
  <div>
    <ul>
      <li>
        <b>Objetivo principal:</b>
        <ul>
          <li>Reducir tiempos de entrega de software de calidad</li>
        </ul>
      </li>
      <li>
        <b>Rompe las barreras entre:</b>
        <ul>
          <li>Desarrollo (Dev) 👨‍💻</li>
          <li>Operaciones (Ops) 🔧</li>
        </ul>
      </li>
    </ul>
  </div>
  <div class="flex justify-center items-center">
    <div class="text-center">
      <div class="text-8xl mb-4">🤝</div>
      <p class="text-lg font-semibold">Dev + Ops = DevOps</p>
      <div class="mt-4 text-sm text-gray-600 italic">"You build it, you run it"</div>
    </div>
  </div>
</div>

<!-- integración continua a lo salvaje -->

---

# DevOps en la Práctica: Ejemplo

<div grid="~ cols-2 gap-6" m="t-5">
  <div>
  
```mermaid {scale:0.5}
sequenceDiagram
    participant Dev as 👨‍💻 Developer
    participant Git as 📚 Git Repository
    participant CI as 🔄 CI/CD Pipeline
    participant Test as 🧪 Test Environment
    participant Prod as 🌐 Production
    participant Monitor as 📊 Monitoring
    
    Dev->>Git: Check-in change
    Git->>CI: Trigger pipeline
    CI->>CI: Build aplication
    CI->>CI: Execute tests
    CI->>Test: Deploy to test env
    CI->>CI: Integration tests
    CI->>Prod: Deploy to production
    Prod->>Monitor: Send usage metrics
    Monitor->>Dev: Alerts and feedback
```
  </div>
</div>

<div class="absolute top-1/2 right-15 -translate-y-1/2 bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-2 rounded shadow-lg max-w-60 text-md z-10 text-center">
  <b>Integración Continua</b> (CI) <br> + <br> <b>Despliegue Continuo</b> (CD)
</div>

<div class="absolute bottom-5 right-5 flex justify-center items-center z-10">
  <div class="bg-gradient-to-r from-green-100 to-blue-100 border-l-4 border-green-500 text-green-700 p-3 rounded shadow-lg max-w-xs text-sm text-center">
    <div class="text-xl mb-1">🤖</div>
    <div class="font-bold mb-1">Automatización total</div>
    <div class="text-xs text-gray-700 font-semibold mb-1">Del commit a producción</div>
    <div class="mt-1 text-base">✨ 🚀 ⚡</div>
  </div>
</div>

<!-- A/B testing -->

---

# Herramientas del Ecosistema DevOps

<br>

<div grid="~ cols-3 gap-4" m="t-5">
  <div>
    <h4 class="text-blue-600 font-bold">🔧 Desarrollo</h4>
    <ul class="text-sm">
      <li>Git, GitHub, GitLab</li>
      <li>IDE/Editors</li>
      <li>Jira, Trello</li>
    </ul>
  </div>
  
  <div>
    <h4 class="text-green-600 font-bold">🏗️ Build & CI/CD</h4>
    <ul class="text-sm">
      <li>Jenkins, GitHub Actions</li>
      <li>GitLab CI, Azure DevOps</li>
      <li>Travis CI, CircleCI</li>
    </ul>
  </div>
  
  <div>
    <h4 class="text-purple-600 font-bold">🧪 Testing</h4>
    <ul class="text-sm">
      <li>JUnit, Jest, Selenium</li>
      <li>SonarQube</li>
      <li>Postman, Newman</li>
    </ul>
  </div>
  
  <div>
    <h4 class="text-orange-600 font-bold">📦 Containerización</h4>
    <ul class="text-sm">
      <li>Docker</li>
      <li>Kubernetes</li>
      <li>Helm</li>
    </ul>
  </div>
  
  <div>
    <h4 class="text-red-600 font-bold">☁️ Cloud & Infraestructura</h4>
    <ul class="text-sm">
      <li>AWS, Azure, GCP</li>
      <li>Terraform, Ansible</li>
      <li>Vagrant</li>
    </ul>
  </div>
  
  <div>
    <h4 class="text-indigo-600 font-bold">📊 Monitorización</h4>
    <ul class="text-sm">
      <li>Prometheus, Grafana</li>
      <li>ELK Stack</li>
      <li>New Relic, Datadog</li>
    </ul>
  </div>
</div>

<div class="mt-6 text-center">
  <p class="text-sm text-gray-600">🎯 El objetivo no es usar todas las herramientas, sino elegir las que mejor se adapten a tu contexto</p>
</div>

---

# Integración / Despliegue Continuo

<div grid="~ cols-2 gap-6" m="t-6">
  <Definicion title="Integración Continua (CI)" emoji="🔄">
    Práctica de integrar cambios de código de forma frecuente en un repositorio compartido,
    ejecutando automáticamente build y pruebas para detectar errores lo antes posible.
  </Definicion>

  <Definicion title="Despliegue Continuo (CD)" emoji="🚀">
    Práctica de publicar automáticamente en producción cada cambio que supera las validaciones
    del pipeline, sin intervención manual en la fase de despliegue.
  </Definicion>
</div>

--- 

# Github Actions

GitHub Actions es la plataforma de automatización de GitHub para definir workflows (CI/CD) en YAML que se ejecutan en respuesta a eventos del repositorio.

<div grid="~ cols-3 gap-4" m="t-5">
  <div>
    <h4 class="text-blue-600 font-bold">⚙️ Workflows</h4>
    <p class="text-sm">Un proceso que ejecuta jobs cuando ocurre un evento.</p>
  </div>

  <div>
    <h4 class="text-green-600 font-bold">📣 Events</h4>
    <p class="text-sm">Actividad que lanza un workflow (push, pull_request, schedule, etc.).</p>
  </div>

  <div>
    <h4 class="text-purple-600 font-bold">🧩 Jobs</h4>
    <p class="text-sm">Conjunto de steps que se ejecutan en un runner (en paralelo o en secuencia).</p>
  </div>

  <div>
    <h4 class="text-teal-600 font-bold">🪜 Steps</h4>
    <p class="text-sm">Pasos individuales dentro de un job. Pueden ser un shell script o un Action.</p>
  </div>

  <div>
    <h4 class="text-orange-600 font-bold">🔨 Actions</h4>
    <p class="text-sm">Acciones reutilizables que encapsulan tareas (publicadas en Marketplace o locales).</p>
  </div>

  <div>
    <h4 class="text-red-600 font-bold">🏃‍♂️ Runners</h4>
    <p class="text-sm">Máquinas (hosted o self-hosted) donde se ejecutan los jobs y sus steps.</p>
  </div>
</div>

<InfoBox content="Cada workflow se define con un archivo <code>*.yml</code> en el directorio <code>.github/workflows/</code> del repositorio, que especifica eventos, jobs, steps, etc."/>

---

# Github Actions

