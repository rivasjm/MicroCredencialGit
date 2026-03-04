---
applyTo: '**/*.md'
---

## Project Context:
   - This project is a presentation built using [Slidev](https://sli.dev/).
   - The main slides are in `slides.md`.
   - Components can be found in the `components/` directory, and are made with Vue.
   - The slides are for a Spanish language course on ci/cd with github actions, so the content of the slides should be in Spanish and related to that topic.
   - For images do not use URLs, use emojis instead.
   - Each slide has limited space, so always prioritize the most important information and be precise.

## Coding Guidelines:
   - The syntax is Markdown, so prioritize using Markdown syntax and slidev directives. If the request cannot be fulfilled with Markdown or built-in slidev directives, use HTML as a fallback.
   - The HTML is styled via UnoCSS which is an Atomic CSS framework similar to Tailwind CSS. You can write HTML inside the markdown and use the UnoCSS classes to style that HTML.
   - Mermaid code cannot be indented.
   - If a two column layout is requested, favor this syntax: <div grid="~ cols-2 gap-2" m="t-5">
   - You can center things with <div class="flex justify-center">...</div>
   - If you are requested to add a note in an absolute position, use the following syntax: <div class="absolute bottom-5 right-5 bg-red-100 border-l-4 border-red-500 text-red-700 p-4 rounded shadow-lg max-w-xs text-sm z-10">. Just change the color and position as the user requests. 
   - For inline code inside another tag do not use backticks, use a code tag.
   - A mermaid diagram can be scaled with this syntax for 80%: ```mermaid {scale:0.8}
   - If you are requested to a definition, use the custom Definicion component, which is used like this: <Definicion title="Mi Título" emoji="📚">Contenido de la definición</Definicion>
   - There is a compact version of the Definicion component called DefinicionCompacta, which is used like this: <DefinicionCompacta title="Mi Título" emoji="📚">Contenido de la definición</DefinicionCompacta>
