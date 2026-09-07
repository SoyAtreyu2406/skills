# txt-notes

Skill para reescribir, organizar y formatear anotaciones personales en texto plano (`.txt`). Mejora claridad y redacción, agrupa conceptos relacionados y aplica una gramática visual consistente, compacta y jerárquica, preservando siempre la información y los datos técnicos.

## Uso

Pedile a la AI que formatee un archivo `.txt` usando la skill. Por ejemplo:

> Dale formato al archivo notas.txt usando la skill txt-notes

La AI va a leer el archivo, reescribir el contenido para mejorarlo y aplicar el formato visual con los símbolos definidos.

## Símbolos

| Símbolo | Significado | Uso |
|---------|-------------|-----|
| `◆` | Título principal | Encabezado del documento |
| `▌` | Sección principal | Bloque temático independiente |
| `▪` | Subsección | División dentro de una sección |
| `[ ]` | Tarea pendiente | Algo que hay que hacer |
| `[x]` | Tarea completada | Algo que ya se hizo |
| `◐` | Tarea en progreso | Algo que está en curso |
| `→` | Idea / acción / relación | Propuestas, consecuencias, aclaraciones |
| `!` | Información importante | Advertencias o datos críticos |
| `?` | Pregunta | Cuestiones que requieren investigación |
| `$` | Comando ejecutable | Comandos de terminal |
| `>` | Salida de comando | Resultado de ejecutar un comando |
| `🔗` | URL independiente | Enlaces que aparecen solos |
| `-` | Elemento de lista | Items informativos |

## Ejemplo

### Antes

```text
Estoy armando una aplicación web para gestionar productos y pedidos. El frontend sería con Astro y Symfony quedaría para el backend. No sé todavía si hace falta React.

Las tecnologías que estoy considerando son Node.js v22.14.0, npm 10.9.2, Astro, Symfony, Tailwind, Git y MySQL. Tailwind todavía no está instalado y Symfony tampoco.

Crear la carpeta del proyecto y el repositorio Git ya está hecho. Todavía falta instalar Node.js, crear el proyecto Astro, instalar Symfony, instalar Tailwind, configurar MySQL y probar el acceso desde otra PC.
```

### Después

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  APLICACIÓN WEB · PRODUCTOS Y PEDIDOS
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

▌ ARQUITECTURA

  Estoy armando una aplicación web para gestionar productos y pedidos. El frontend sería con Astro y Symfony quedaría para el backend. No sé todavía si hace falta React.

  → ¿Realmente necesito React?


▌ TECNOLOGÍAS

  Las tecnologías que estoy considerando son:

  - Node.js v22.14.0
  - npm 10.9.2
  - Astro
  - Symfony
  - Tailwind
  - Git
  - MySQL

  Tailwind todavía no está instalado, Symfony tampoco y Node.js tampoco.


▌ ESTADO ACTUAL

  [x] Crear la carpeta del proyecto
  [x] Crear el repositorio Git

  [ ] Instalar Node.js
  [ ] Crear el proyecto Astro
  [ ] Instalar Symfony
  [ ] Instalar Tailwind
  [ ] Configurar MySQL
  [ ] Probar acceso desde otra PC
```
