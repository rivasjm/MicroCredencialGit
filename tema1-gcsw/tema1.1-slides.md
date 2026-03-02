

# Índice

<br>

1. <span style="color: red; font-weight: bold;">Gestión de la configuración software</span>  
2. Control de versiones con Git  
3. Modelos organizativos con Git  

---

# Gestión de la Configuración de Sistemas Software

<Definicion title="Gestión de la Configuración" emoji="🛠️">
  La gestión de la configuración se ocupa de las políticas, procesos y herramientas para gestionar los cambios en los <b>sistemas software</b>.
</Definicion>

<div grid="~ cols-2 gap-2" m="t-5">
  <div>
    <ul>
      <li>
        <b>¿Por qué necesitas gestión de configuración?</b>
        <ul>
          <li>Es fácil perder el control de los cambios y versiones de componentes incorporados en cada versión del sistema.</li>
          <li>Es esencial en proyectos en equipo para controlar los cambios realizados por diferentes desarrolladores.</li>
        </ul>
      </li>
    </ul>
  </div>
  <div class="flex justify-center">
    <span class="text-6xl">👥</span>
  </div>
</div>

<!-- Software Configuration Management en ingles (SCM). ¿Qué cosas son cambiantes? -> ciclo de vida -->

---

# ¿Qué queremos evitar?

<div grid="~ cols-2 gap-2" m="t-5">
  <div>
    <ul>
      <li>
        <b>Evitar el caos en el desarrollo</b>
        <ul>
          <li>Desorden en archivos y versiones.</li>
          <li>Dificultad para saber qué ha cambiado y quién lo ha hecho.</li>
          <li>Confusión y errores al integrar cambios.</li>
        </ul>
      </li>
    </ul>
  </div>
  <div class="flex justify-center">
    <span class="text-7xl">🧩</span>
  </div>
</div>

<div class="flex justify-center mt-4">
  <img src="/images/mess.png" alt="Desorden en el desarrollo" class="w-192 rounded" />
</div>

---

# ¿Por qué necesitamos Gestión de la Configuración? 

<br>

<div grid="~ cols-2 gap-4" m="t-4">
  <div class="bg-blue-50 p-4 rounded shadow text-center">
    <span class="text-4xl mb-2 block">⏸️</span>
    <div class="font-bold mb-1">¿Cómo hago como si no hubiese pasado nada?</div>
    <div class="text-sm text-gray-700">Recuperar el estado anterior del sistema ante errores o cambios no deseados.</div>
  </div>
  <div class="bg-green-50 p-4 rounded shadow text-center">
    <span class="text-4xl mb-2 block">👥</span>
    <div class="font-bold mb-1">¿Cómo gestiono a dos personas trabajando en el mismo archivo?</div>
    <div class="text-sm text-gray-700">Gestionar los cambios realizados por varios usuarios al mismo tiempo.</div>
  </div>
  <div class="bg-yellow-50 p-4 rounded shadow text-center">
    <span class="text-4xl mb-2 block">🔍</span>
    <div class="font-bold mb-1">¿Qué diferencias hay entre versiones?</div>
    <div class="text-sm text-gray-700">Identificar y comparar los cambios entre distintas versiones de archivos.</div>
  </div>
  <div class="bg-red-50 p-4 rounded shadow text-center">
    <span class="text-4xl mb-2 block">📋</span>
    <div class="font-bold mb-1">Problema de la copia correcta</div>
    <div class="text-sm text-gray-700">Facilitar la identificación de la versión correcta.</div>
  </div>
</div>



---

# Gestión de la Configuración dentro del Ciclo de Vida


<div class="flex justify-center mt-4">
  <img src="/images/ciclo-de-vida.svg" alt="Ciclo de vida de la gestión de configuración" class="max-h-96 rounded shadow" />
</div>

---

# Gestión de la Configuración dentro del Ciclo de Vida


<div class="flex justify-center mt-4">
  <img src="/images/ciclo-de-vida-gc.svg" alt="Ciclo de vida de la gestión de configuración" class="max-h-96 rounded shadow" />
</div>

---

# Conceptos Clave

<div grid="~ cols-2 gap-2" style="grid-template-columns: 1fr 1fr;">
  <DefinicionCompacta title="Ítem de Configuración" emoji="📦">
    Elemento gestionado de manera individual en el sistema, como fichero de código fuente, documentación, ficheros de configuración, binarios, etc.
  </DefinicionCompacta>
  <DefinicionCompacta title="Versión" emoji="🔢">
    Instancia de un ítem de configuración que difiere de alguna manera de otras instancias del mismo ítem.
  </DefinicionCompacta>
</div>

<div grid="~ cols-2 gap-2" style="grid-template-columns: 1fr 1fr;">
  <DefinicionCompacta title="Baseline" emoji="📏">
    Conjunto de versiones de ítems de configuración que representa un estado significativo, claramente identificado, y aprobado, del sistema.
  </DefinicionCompacta>
  <DefinicionCompacta title="Mainline" emoji="🛤️">
    Secuencia de <em>Baselines</em> a lo largo del tiempo. Evolución de versiones significativas (rama<code>main</code>)
  </DefinicionCompacta>
</div>

<div class="flex justify-center">
  <DefinicionCompacta title="Release" emoji="🚀">
    Versión del sistema (un <em>Baseline</em>), o de un ítem de configuración concreto, que se distribuye a los usuarios finales o clientes.
  </DefinicionCompacta>
</div>

<!-- ejemplo de tabla con items y versiones -->

--- 

# Areas de la Gestión de la Configuración

<br>
<br>

```mermaid
graph LR
    subgraph Gestión de cambios
        A1["📄<br>Petición de Cambio"]
        A2["Bugzilla<br>JIRA<br>Trello<br>Backlog"]
    end

    subgraph Gestión de versiones
        B1["📑<br>Versiones Software"]
        B2["Git<br>Svn<br>Mercurial"]
    end

    subgraph Construcción de sistemas
        C1["⚙️<br>Sistema Executable"]
        C2["Maven<br>Gradle<br>Jenkins<br>Travis<br>Github Actions"]
    end

    subgraph Gestión de lanzamientos
        D1["🎯<br>Versión Operativa"]
        D2["App Store<br>Google Play<br>Steam"]
    end

    %% Conexiones entre las etapas del proceso
    A1 -- " " --> B1 -- " " --> C1 -- " " --> D1

    %% Estilos
    classDef area fill:#e0f7fa,stroke:#00796b,stroke-width:2px,color:#004d40
    classDef tools fill:#455a64,color:#eceff1,stroke:#263238,stroke-width:2px

    class A1,B1,C1,D1 area
    class A2,B2,C2,D2 tools
```
---

# Sistema de desarrollo 

<br>

```mermaid {scale:0.8}
graph LR
    subgraph "💻 Development System"
        direction TB
        DevTools["Development<br>Tools"]
        Workspace["Private<br>Workspace"]
    end

    subgraph "Version&nbsp;Control&nbsp;Build&nbsp;Server"
        VMS["Version<br>Management System"]
        BS["Build<br>Server"]
        VMS -- "check-out" --> BS
    end

    subgraph "🎯 Target System"
        direction TB
        Executable["Executable<br>System"]
        Platform["Target<br>Platform"]
    end

    %% Flujo principal
    Workspace -- "check-in" --> VMS
    VMS -- "check-out" --> Workspace
    BS --> Platform

    %% Estilos para cada sistema
    classDef devSystem fill:#fff3e0,stroke:#f57c00,stroke-width:3px,color:#e65100
    classDef versionSystem fill:#f3e5f5,stroke:#7b1fa2,stroke-width:3px,color:#4a148c
    classDef targetSystem fill:#e8f5e8,stroke:#388e3c,stroke-width:3px,color:#1b5e20

    class DevTools,Workspace devSystem
    class VMS,BS versionSystem
    class Executable,Platform targetSystem
```
<br>
<div class="text-m">

- **Check-out**: Se obtiene una versión del sistema (un *baseline*).
- **Check-in**: El desarrollador envía sus cambios desde su espacio de trabajo privado al sistema de control de versiones (nueva versión).

</div>

---

# Integración Continua

<br>

<div grid="~ cols-2 gap-2" m="t-5">
  <div>
    <ul>
      <li>
        <b>¿Qué es la integración continua?</b>
        <ul>
          <li>Integrar frecuentemente los cambios de todos los desarrolladores en el servidor.</li>
          <li>Integración con pruebas automáticas.</li>
          <li>Permite detectar errores rápidamente y mantener el sistema siempre en un estado funcional.</li>
        </ul>
      </li>
      <li>
        <b>Herramientas habituales:</b>
        <ul>
          <li>Jenkins, GitHub Actions, GitLab CI, Travis CI</li>
        </ul>
      </li>
    </ul>
  </div>
  <div class="flex justify-center">
    <div>
      <img src="/images/ci.png" alt="Integración Continua" class="max-h-84 rounded shadow" />
      <p class="text-right text-xs mt-2">Figura obtenida de <b>Software Engineering</b>, 10th Edition, Ian Sommerville</p>
    </div>
  </div>
</div>

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