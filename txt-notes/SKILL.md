---

name: personal-notes
description: Formatea y organiza notas personales en archivos TXT con una estructura visual consistente, clara y compacta. Clasifica automáticamente títulos, secciones, subsecciones, tareas, ideas, URLs, comandos, código, configuración, tablas y otros contenidos sin modificar su significado.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Personal Notes

Formatea notas personales `.txt` manteniendo **todo el contenido original**, pero mejorando su estructura, jerarquía, legibilidad y consistencia visual.

El resultado debe parecer una **nota personal cuidadosamente organizada**, no un documento Markdown ni una página web.

---

# REGLAS PRINCIPALES

1. No eliminar información.
2. No inventar información.
3. No cambiar el significado.
4. No convertir automáticamente todo en listas.
5. Clasificar cada contenido antes de formatearlo.
6. Mantener una estructura visual consistente.
7. Usar indentación para representar jerarquía.
8. Evitar decoración innecesaria.
9. No utilizar líneas horizontales como separadores generales.
10. Las URLs, comandos y salidas de comandos deben distinguirse claramente.

---

# GRAMÁTICA VISUAL

Utilizar únicamente estos símbolos:

```text
◆  = título/documento principal
▌  = sección
▪  = subsección
[ ] = tarea pendiente
[x] = tarea completada
◐  = tarea en progreso
→  = idea / acción
!  = importante
?  = pregunta / investigar
$  = comando ejecutable
>  = salida de comando
🔗 = URL / enlace
```

No inventar otros símbolos para representar categorías.

---

# TÍTULO PRINCIPAL

El primer título importante del documento debe utilizar este formato:

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  TÍTULO PRINCIPAL · FECHA
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Ejemplo:

Entrada:

```text
◆ PLAN DE PROYECTO PASTELERÍA · Astro + Tailwind + OpenCode + Symfony + Mercado Pago
```

Salida:

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  PLAN DE PROYECTO PASTELERÍA · Astro + Tailwind + OpenCode + Symfony + Mercado Pago
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

La línea horizontal solamente está permitida como parte del título principal.

No utilizar este formato para las secciones.

---

# SECCIONES

Los títulos principales de cada bloque deben utilizar:

```text
▌ NOMBRE DE SECCIÓN
```

Ejemplo:

```text
▌ OBJETIVO

  Crear una web moderna y responsive para una pastelería.
```

No utilizar:

```text
▌ OBJETIVO:
▌ OBJETIVO ----
▌ OBJETIVO ────
```

---

# SUBSECCIONES

Las subdivisiones dentro de una sección utilizan:

```text
  ▪ NOMBRE
```

Ejemplo:

```text
▌ STACK

  ▪ Frontend

    Astro
    Tailwind CSS
    JavaScript / TypeScript

  ▪ Backend

    Symfony
    Doctrine
```

Una subsección no debe terminar en `:`.

Transformar:

```text
▪ Frontend:
```

en:

```text
▪ Frontend
```

Cuando una subsección contiene información debajo, dejar una línea en blanco antes del contenido.

---

# INDENTACIÓN

Utilizar esta jerarquía:

```text
▌ SECCIÓN

  ▪ SUBSECCIÓN

    Contenido
```

Para contenido directamente perteneciente a una sección:

```text
▌ OBJETIVO

  Contenido de la sección.
```

Para listas:

```text
▌ TECNOLOGÍAS

  Astro
  Tailwind CSS
  Symfony
```

No utilizar indentación excesiva.

---

# TAREAS

Las tareas pendientes utilizan:

```text
[ ] Tarea pendiente
```

Las tareas completadas:

```text
[x] Tarea completada
```

Las tareas en progreso:

```text
◐ Tarea en progreso
```

Ejemplo:

```text
▌ PENDIENTES

  [ ] Instalar Node.js
  [ ] Crear proyecto Astro
  [ ] Configurar Tailwind
```

No convertir tareas en párrafos.

---

# IDEAS Y ACCIONES

Las ideas o acciones que no sean tareas formales utilizan:

```text
→ Idea o acción
```

Ejemplo:

```text
▌ IDEAS

  → Reorganizar el proyecto
  → Probar una estructura diferente
```

---

# IMPORTANTE

Información que requiere atención utiliza:

```text
! Texto importante
```

Ejemplo:

```text
▌ IMPORTANTE

  ! Por ahora comenzar SOLO con frontend.
```

No utilizar `!` para información normal.

---

# PREGUNTAS

Las preguntas o cosas que necesitan investigación utilizan:

```text
? Pregunta o tema a investigar
```

Ejemplo:

```text
▌ INVESTIGAR

  ? ¿Conviene utilizar SSR?
  ? ¿Cómo desplegar el proyecto?
```

---

# URLs

Una URL independiente **siempre** utiliza:

```text
🔗 URL
```

Nunca utilizar `$`, `>`, `→` ni `[ ]` para una URL independiente.

Una línea que comience con:

```text
http://
https://
www.
```

debe considerarse una URL, salvo que forme parte explícita de código, configuración o salida de un comando.

## Ejemplo obligatorio

Entrada:

```text
▪ URL habitual:
http://localhost:4321
```

Salida:

```text
  ▪ URL habitual

    🔗 http://localhost:4321
```

Otro ejemplo:

```text
▪ Sitio web:
https://example.com
```

debe convertirse en:

```text
  ▪ Sitio web

    🔗 https://example.com
```

No utilizar:

```text
$ http://localhost:4321
> http://localhost:4321
→ http://localhost:4321
```

---

# COMANDOS

Un comando ejecutable utiliza `$`.

Ejemplo:

```text
▌ COMANDOS

  $ npm install
  $ npm run dev
  $ git status
```

El símbolo `$` solamente debe utilizarse cuando realmente se trata de un comando ejecutable.

Una URL nunca es un comando.

---

# SALIDA DE COMANDOS

La salida producida por un comando utiliza `>`.

Ejemplo:

```text
  $ node --version

  > v22.14.0
```

No confundir salida de comando con una URL.

---

# CÓDIGO

Los bloques de código deben conservar su sintaxis y estructura.

Utilizar una subsección indicando el lenguaje:

```text
▌ CÓDIGO · JS

  ▪ Función principal

    const total = precio * cantidad;
    return total;
```

Lenguajes habituales:

```text
▌ CÓDIGO · JS
▌ CÓDIGO · PHP
▌ CÓDIGO · SQL
▌ CÓDIGO · JSON
▌ CÓDIGO · TYPESCRIPT
```

No modificar código para hacerlo más "bonito".

---

# CONFIGURACIÓN

Para archivos o fragmentos de configuración:

```text
▌ CONFIG · ENV
▌ CONFIG · YAML
▌ CONFIG · JSON
```

Mantener los valores y estructura originales.

---

# TABLAS Y COMPARACIONES

Las tablas ASCII pueden utilizar líneas horizontales.

Ejemplo:

```text
  Symfony                  Astro
  ────────────────────────────────────────
  templates/               src/pages/
  Twig                     .astro
  include                  Component
  base.html.twig           Layout
  Routing                  pages/
  public/                  public/
```

Las líneas horizontales están permitidas dentro de tablas o comparaciones.

No convertir una tabla en una lista si la estructura comparativa aporta información.

---

# ÁRBOLES DE DIRECTORIOS

Mantener los árboles de archivos como estructuras visuales.

Ejemplo:

```text
  frontend/
  ├── public/
  ├── src/
  │   └── pages/
  │       └── index.astro
  ├── astro.config.mjs
  ├── package.json
  └── tsconfig.json
```

No reemplazar el árbol por una lista.

---

# TEXTO NORMAL

Los párrafos normales deben quedar debajo de su sección:

```text
▌ OBJETIVO

  Crear una web moderna y responsive para una pastelería.

  El proyecto comienza como frontend y sirve también como proyecto
  de aprendizaje.
```

Mantener los párrafos separados cuando sean ideas diferentes.

---

# REGLA ESPECIAL PARA ETIQUETAS

Cuando una línea funciona como nombre de una subsección, eliminar los dos puntos finales.

Transformar:

```text
▪ Frontend:
▪ Backend:
▪ URL habitual:
▪ Objetivo:
```

en:

```text
▪ Frontend
▪ Backend
▪ URL habitual
▪ Objetivo
```

Los dos puntos pueden mantenerse dentro de texto normal cuando formen parte del contenido.

---

# NO CONFUNDIR CATEGORÍAS

Aplicar estas reglas en este orden:

```text
URL independiente
        ↓
comando
        ↓
salida de comando
        ↓
código/configuración
        ↓
tarea
        ↓
idea/acción
        ↓
pregunta
        ↓
texto normal
```

Ejemplos:

```text
http://localhost:4321
```

→ URL:

```text
🔗 http://localhost:4321
```

```text
npm run dev
```

→ comando:

```text
$ npm run dev
```

```text
Servidor iniciado en localhost
```

→ salida solamente si realmente corresponde a la salida de un comando:

```text
> Servidor iniciado en localhost
```

---

# ESTRUCTURA RECOMENDADA

Cuando el contenido lo permita, utilizar una estructura similar a:

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  TÍTULO · FECHA
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

▌ OBJETIVO

  Texto.


▌ STACK

  ▪ Frontend

    Astro
    Tailwind CSS

  ▪ Backend

    Symfony
    Doctrine


▌ PENDIENTES

  [ ] Tarea
  [ ] Tarea


▌ IMPORTANTE

  ! Información importante


▌ IDEAS

  → Idea


▌ INVESTIGAR

  ? Pregunta


▌ COMANDOS

  $ npm install


▌ URL

  🔗 http://localhost:4321
```

No es obligatorio crear todas estas secciones. Utilizar solamente las que correspondan al contenido original.

---

# PRESERVACIÓN DEL CONTENIDO

El objetivo es **reformatear**, no reescribir.

No:

* resumir
* eliminar información
* inventar tareas
* inventar fechas
* inventar URLs
* agregar tecnologías
* cambiar nombres
* cambiar comandos
* modificar código
* agregar conclusiones que no existían

Sí:

* ordenar visualmente
* agrupar contenido relacionado
* crear secciones cuando la estructura sea evidente
* crear subsecciones cuando exista una jerarquía clara
* convertir etiquetas en subsecciones
* identificar URLs
* identificar comandos
* identificar tareas
* mejorar la indentación

---

# ANTI-DECORACIÓN

No utilizar:

```text
════════════════════════════
----------------------------
____________________________
********************************
################################
```

como separadores decorativos entre secciones.

La única excepción es:

1. el título principal;
2. líneas necesarias dentro de tablas o comparaciones.

No agregar emojis adicionales.

El único emoji permitido por esta Skill es:

```text
🔗
```

para URLs.

---

# CONTROL DE CALIDAD

Antes de entregar el TXT final comprobar:

* ¿Existe un título principal con `◆━━━━`?
* ¿Las secciones utilizan `▌`?
* ¿Las subsecciones utilizan `▪`?
* ¿Las subsecciones no terminan en `:`?
* ¿Las tareas utilizan `[ ]`, `[x]` o `◐`?
* ¿Las ideas utilizan `→`?
* ¿Lo importante utiliza `!`?
* ¿Las preguntas utilizan `?`?
* ¿Los comandos utilizan `$`?
* ¿La salida de comandos utiliza `>`?
* ¿Las URLs independientes utilizan `🔗`?
* ¿Las URLs NO utilizan `$`?
* ¿Las tablas conservan sus líneas horizontales?
* ¿No existen separadores decorativos innecesarios?
* ¿Se conservó todo el contenido original?
* ¿La indentación refleja correctamente la jerarquía?

Si alguna regla entra en conflicto con otra, priorizar:

```text
preservar contenido
    ↓
clasificar correctamente
    ↓
mantener jerarquía
    ↓
aplicar gramática visual
    ↓
evitar decoración innecesaria
```

# REGLA FINAL

El resultado debe parecer una **nota personal organizada, clara y visualmente consistente**, utilizando pocos elementos pero de manera muy precisa.

**Clasificar primero. Formatear después. No inventar. No eliminar.**




