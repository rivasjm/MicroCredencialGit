

# Índice

<br>

1. Gestión de la configuración software  
2. Control de versiones con Git  
3. <span style="color: red; font-weight: bold;">Modelos organizativos con Git</span>  

---

# Centralizado Clásico

<div class="flex justify-center" m="t-10">
  
```mermaid {scale:1}
flowchart TD
    A[Repositorio<br>central<br>📦]:::repo
    B(Repositorio<br>local<br>👩‍💻):::dev
    C(Repositorio<br>local<br>👨‍💻):::dev
    D(Repositorio<br>local<br>👩‍💻):::dev
    B -- "push" --> A
    A -- "pull" --> B
    C -- "push" --> A
    A -- "pull" --> C
    D -- "push" --> A
    A -- "pull" --> D
    classDef repo fill:#eab308,color:#fff,stroke:#b45309,stroke-width:2px
    classDef dev fill:#f87171,color:#fff,stroke:#b91c1c,stroke-width:2px
```
</div>

<div class="absolute bottom-5 right-5 bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4 rounded shadow-lg max-w-xl text-sm z-10">
  Modelo tradicional y habitual. Hay un único repositorio central donde todos los desarrolladores sincronizan su trabajo (push/pull).
</div>

<!-- https://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows -->

---

# Modelo de Integrador Destacado

<div class="flex justify-center" m="t-4">
  <img src="/images/integrador-destacado.svg" alt="Modelo de Integrador Destacado" class="w-2/3 rounded shadow-lg" />
</div>

<div class="absolute bottom-5 right-5 bg-blue-100 border-l-4 border-blue-500 text-blue-700 p-4 rounded shadow-lg max-w-md text-sm z-10">
  Este es el modelo de <b>GitHub</b>: cada desarrollador trabaja en su propio <b>Fork</b> (repositorio público personal), y propone cambios mediante <b>Pull Requests</b> al repositorio principal.
</div>

<!-- https://git-scm.com/book/en/v2/GitHub-Forks-Branches-and-Merges-in-a-Nutshell -->

---

# Modelo Dictador y Tenientes

<div class="flex justify-center" m="t-4">
  <img src="/images/dictador-tenientes.svg" alt="Modelo Dictador y Tenientes" class="w-2/3 rounded shadow-lg" />
</div>

<div class="absolute bottom-5 right-5 bg-green-100 border-l-4 border-green-500 text-green-700 p-4 rounded shadow-lg max-w-xl text-sm z-10">
  En este modelo, un <b>Dictador</b> (mantenedor principal) integra los cambios propuestos por un grupo reducido de <b>Tenientes</b>, quienes a su vez reciben contribuciones del resto de desarrolladores.
</div>

<div class="absolute bottom-60 left-10 w-1/8">
  <div>
    <img src="https://cdn.britannica.com/99/124299-050-4B4D509F/Linus-Torvalds-2012.jpg" alt="Modelo Dictador y Tenientes" class="w-full rounded shadow-lg" />
  </div>
</div>

---

# Git Flow

<div grid="~ cols-2 gap-2" m="t-4">

<div>

```mermaid {scale:0.7}
gitGraph
    commit id: "Initial"
    branch develop
    checkout develop
    commit id:" "
    
    branch feature/login
    checkout feature/login
    commit id: "Login A"
    commit id: "Login B"
    checkout develop
    merge feature/login
    
    branch feature/ui
    checkout feature/ui
    commit id: "UI A"
    checkout develop
    merge feature/ui

    checkout develop
    branch release/1.0
    checkout release/1.0
    commit id: "Corrección 1"
    commit id: "Corrección 2"
    checkout main
    merge release/1.0 tag: "v1.0"
    checkout develop
    merge release/1.0
```

</div>

<div flex="~ col" class="text-base items-end text-right">
  <DefinicionCompacta title="main" emoji="🚀">Rama de producción, siempre estable.</DefinicionCompacta>
  <DefinicionCompacta title="develop" emoji="🛠️">Rama de integración de desarrollo.</DefinicionCompacta>
  <DefinicionCompacta title="feature/*" emoji="✨">Nuevas funcionalidades o mejoras.</DefinicionCompacta>
  <DefinicionCompacta title="release/*" emoji="🔖">Preparación de una nueva versión estable.</DefinicionCompacta>
</div>

</div>

<div class="absolute bottom-5 left-5 bg-gray-100 border-l-4 border-gray-500 text-gray-700 p-4 rounded shadow-lg max-w-md text-xs z-10">
  Referencia original: <a href="https://nvie.com/posts/a-successful-git-branching-model/" target="_blank" class="underline text-blue-700">nvie.com/posts/a-successful-git-branching-model/</a>
</div>

---

# Git Flow: Hotfix

<div grid="~ cols-2 gap-2" m="t-4">

<div>

```mermaid {scale:0.9}
gitGraph
    commit id: "v1.0"
    branch develop

    branch hotfix/1.0.1
    checkout hotfix/1.0.1
    commit id: "Corrección urgente"
    checkout main
    merge hotfix/1.0.1 tag: "v1.0.1"
    checkout develop
    merge hotfix/1.0.1

    checkout main
    commit id: "Commit extra en main"
    branch hotfix/1.0.2
    checkout hotfix/1.0.2
    commit id: "Segundo hotfix"
    checkout main
    merge hotfix/1.0.2 tag: "v1.0.2"
    checkout develop
    merge hotfix/1.0.2
```

</div>

<div flex="~ col" class="text-base items-end text-right">
  <DefinicionCompacta title="main" emoji="🚀">Rama de producción, siempre estable.</DefinicionCompacta>
  <DefinicionCompacta title="hotfix/*" emoji="🧯">Corrección urgente sobre producción.</DefinicionCompacta>
</div>

</div>

<div class="absolute bottom-5 left-5 bg-gray-100 border-l-4 border-gray-500 text-gray-700 p-4 rounded shadow-lg max-w-md text-xs z-10">
  Un <b>hotfix</b> permite corregir errores críticos en producción rápidamente, integrando los cambios tanto en <code>main</code> como en <code>develop</code>, sin necesidad de crear una rama <code>feature</code>.
</div>

---

# Trunk-based Development

<div grid="~ cols-2 gap-2" m="t-10">

<div>

```mermaid {scale:0.9}
gitGraph
    commit id: "Inicio"

    branch feat1
    checkout feat1
    commit id: "Arreglo rápido"
    checkout main
    merge feat1

    branch feat2
    checkout feat2
    commit id: "Funcionalidad A"
    checkout main
    merge feat2

    checkout main
    commit id: "Pequeña mejora"
```

</div>

<div flex="~ col" class="text-base items-end text-right">
  <DefinicionCompacta title="main" emoji="🌳">Rama principal, todos los cambios se integran aquí frecuentemente.</DefinicionCompacta>
  <DefinicionCompacta title="featx" emoji="✨">Ramas de <b>muy corta duración</b> para implementar cambios</DefinicionCompacta>
</div>

</div>

<div class="absolute bottom-5 left-5 bg-green-100 border-l-4 border-green-500 text-green-700 p-4 rounded shadow-lg max-w-xs text-sm z-10">
  Integración continua real: ramas cortas, cambios frecuentes en <code>main</code>.
</div>

