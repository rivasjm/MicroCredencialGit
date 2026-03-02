---
theme: default
background: https://cover.sli.dev
title: CI/CD con GitHub Actions
info: |
  ## Microcredencial: Git y Metodologías Ágiles
  Curso completo de 8 horas sobre Integración y Entrega Continua.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# CI/CD con GitHub Actions

### Microcredencial: Git y Metodologías Ágiles

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Comenzar <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.prev" title="Previous Slide" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:chevron-left />
  </button>
  <button @click="$slidev.nav.next" title="Next Slide" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:chevron-right />
  </button>
</div>

---
layout: section
---

# Módulo 1
## Fundamentos de CI y GitHub Actions (2 horas)

---

# ¿Qué es la Integración Continua (CI)?

La CI es una práctica de desarrollo que requiere que los desarrolladores integren el código en un repositorio compartido varias veces al día.

- **Resolución de conflictos:** Evita el "infierno de la integración" al final del proyecto.
- **Detección temprana:** Los errores se encuentran minutos después de escribir el código.
- **Confianza:** El repositorio principal siempre está en un estado saludable.

> **[IMAGEN: Diagrama del ciclo de CI]**
> *Descripción: Un círculo infinito que muestra las etapas: Plan -> Code -> Build -> Test -> Release (CI para aquí) -> Deploy -> Operate -> Monitor.*

---

# CI vs. CD: Entendiendo la diferencia

| Concepto | Definición | Objetivo |
| --- | --- | --- |
| **CI** (Continuous Integration) | Automatizar Build y Test | Validar cada cambio. |
| **CD** (Continuous Delivery) | Automatizar el empaquetado | Tener un artefacto listo para desplegar. |
| **CD** (Continuous Deployment) | Automatizar el despliegue | Llevar el cambio a producción sin intervención humana. |

---

# Arquitectura de GitHub Actions

GitHub Actions es una plataforma de automatización que permite crear flujos de trabajo (workflows) directamente en tu repositorio.

- **Workflows:** Procesos automatizados configurados en archivos `.yml`.
- **Events:** Disparadores (push, pull_request, schedule).
- **Jobs:** Conjunto de pasos que se ejecutan en el mismo runner.
- **Steps:** Tareas individuales (comandos shell o acciones).
- **Actions:** Aplicaciones reutilizables que realizan tareas complejas.
- **Runners:** Servidores que ejecutan los workflows (Ubuntu, Windows, macOS).

> **[GRÁFICO: Jerarquía de GitHub Actions]**
> *Descripción: Un diagrama de cajas anidadas: Evento -> Workflow -> Job 1 (Runner A) -> Step 1 -> Step 2...*

---

# Ejercicio Práctico 1: Hola Mundo

1. Crear un nuevo repositorio público en GitHub.
2. En la raíz, crear la carpeta `.github/workflows/`.
3. Crear el archivo `hello-world.yml`:

```yaml
name: Mi primer Workflow
on: [push]
jobs:
  saludo:
    runs-on: ubuntu-latest
    steps:
      - name: Decir hola
        run: echo "¡Hola desde GitHub Actions!"
```

4. Hacer `push` y revisar la pestaña **Actions** en GitHub.

---
layout: section
---

# Módulo 2
## Construcción y Pruebas Automatizadas (2 horas)

---

# Configuración del Entorno

Para trabajar con nuestro código, necesitamos preparar el Runner.

- **Checkout:** `actions/checkout@v4` descarga nuestro código en el runner.
- **Setup:** `actions/setup-node`, `actions/setup-python`, `actions/setup-go` instalan el lenguaje necesario.

```yaml
steps:
  - uses: actions/checkout@v4
  - uses: actions/setup-node@v4
    with:
      node-version: '20'
```

---

# Calidad y Pruebas

El corazón de la CI es asegurar que el código cumple con los estándares.

- **Linters:** Analizan el estilo y posibles errores estáticos (ESLint, Flake8).
- **Unit Tests:** Prueban la lógica de las funciones.
- **Exit Codes:** GitHub Actions considera que un paso ha fallado si el comando devuelve un código distinto de `0`.

> **[IMAGEN: Captura de pantalla de GitHub]**
> *Descripción: Una lista de checks en un Pull Request con algunos en verde (check) y uno en rojo (X).*

---

# Ejercicio Práctico 2: Pipeline de Calidad

1. Crear un pequeño proyecto (ej: un archivo JS con una función simple).
2. Configurar un workflow que:
   - Instale dependencias (`npm install`).
   - Ejecute un linter.
   - Ejecute tests.
3. Forzar un fallo en un test, subir el código y observar cómo GitHub bloquea el workflow.
4. Corregir y verificar que el "check" se pone en verde.

---
layout: section
---

# Módulo 3
## Estrategias de Matriz, Caché y Artefactos (2 horas)

---

# Estrategias de Matriz (Matrix)

¿Cómo sabemos si nuestra app funciona en Node 18, 20 y 22 simultáneamente?

```yaml
strategy:
  matrix:
    os: [ubuntu-latest, windows-latest]
    node: [18, 20, 22]
```

Esto generará **6 jobs paralelos** automáticamente.

---

# Optimización con Caché

Instalar dependencias en cada ejecución es lento y consume ancho de banda.

- `actions/cache`: Almacena carpetas (como `node_modules` o `.pip-cache`) entre ejecuciones.
- Si el archivo de bloqueo (`package-lock.json`) no ha cambiado, restaura la carpeta al instante.

> **[GRÁFICO: Comparativa de tiempo con/sin caché]**
> *Descripción: Un gráfico de barras mostrando 2 minutos sin caché frente a 15 segundos con caché.*

---

# Artefactos: Guardando resultados

Los runners son efímeros: al terminar el job, todo se borra.

- **Artifacts:** Archivos generados (binarios, reportes HTML, PDFs) que queremos conservar.
- `actions/upload-artifact`: Sube archivos desde el runner a GitHub.
- `actions/download-artifact`: Descarga artefactos en otros jobs o manualmente.

---

# Ejercicio Práctico 3: Optimización y Matrices

1. Modificar el workflow anterior para usar una matriz de versiones del lenguaje.
2. Implementar caché para las dependencias.
3. Al terminar los tests, generar un reporte y subirlo como artefacto.
4. Comprobar que el tiempo de ejecución disminuye tras la primera pasada.

---
layout: section
---

# Módulo 4
## Entrega y Despliegue Continuo (CD) (2 horas)

---

# Versionado y Releases

El despliegue suele estar ligado a hitos específicos (etiquetas de versión).

- **SemVer:** v1.0.0 (Major.Minor.Patch).
- **Trigger por Tags:**
```yaml
on:
  push:
    tags:
      - 'v*'
```

- **GitHub Releases:** Espacio donde los usuarios descargan las versiones estables.

---

# Gestión de Secretos (Secrets)

**¡NUNCA!** pongas contraseñas o claves API en el código.

1. Ve a `Settings -> Secrets and variables -> Actions`.
2. Crea una variable (ej: `SERVER_PASSWORD`).
3. Úsala en el workflow: `${{ secrets.SERVER_PASSWORD }}`.

GitHub enmascarará el valor en los logs como `***`.

---

# Despliegue a Producción

Existen muchas formas de desplegar:
- **SFTP/SSH:** Para servidores tradicionales.
- **S3/Netlify/Vercel:** Para aplicaciones frontend modernas.
- **Docker:** Para arquitecturas basadas en contenedores.

> **[IMAGEN: Diagrama de flujo de despliegue]**
> *Descripción: Tag 'v1.1' -> CI Workflow -> Build -> SSH Transfer -> Servidor Web actualizado.*

---

# Ejercicio Práctico 4: Despliegue Final

1. Crear una web sencilla (`index.html`).
2. Configurar un workflow que se dispare solo al crear un Tag.
3. Crear una Release automática en GitHub.
4. Usar los **Secrets** para guardar credenciales SSH.
5. Desplegar la web al servidor de la universidad usando `rsync` o una acción de SFTP.

---

# ¡Gracias! ¿Preguntas?

**Recursos adicionales:**
- [Documentación oficial de GitHub Actions](https://docs.github.com/es/actions)
- [GitHub Marketplace](https://github.com/marketplace?type=actions)
- [Slidev Documentation](https://sli.dev)
