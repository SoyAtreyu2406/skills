# Ejemplo: nota de proyecto con estado mezclado

## Antes

```text
Estoy armando una aplicación web para gestionar productos y pedidos. El frontend sería con Astro y Symfony quedaría para el backend. No sé todavía si hace falta React.

Las tecnologías que estoy considerando son Node.js v22.14.0, npm 10.9.2, Astro, Symfony, Tailwind, Git y MySQL. Tailwind todavía no está instalado y Symfony tampoco.

Crear la carpeta del proyecto y el repositorio Git ya está hecho. Todavía falta instalar Node.js, crear el proyecto Astro, instalar Symfony, instalar Tailwind, configurar MySQL y probar el acceso desde otra PC.
```

## Después

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  APLICACIÓN WEB · PRODUCTOS Y PEDIDOS
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Estoy armando una aplicación web para gestionar productos y pedidos. El
frontend sería con Astro y Symfony quedaría para el backend.

? No sé todavía si hace falta React.


▌ TECNOLOGÍAS

  Las tecnologías que estoy considerando son:

  - Node.js v22.14.0
  - npm 10.9.2
  - Astro
  - Symfony
  - Tailwind
  - Git
  - MySQL

  Tailwind todavía no está instalado, Symfony tampoco.


▌ PENDIENTE

  [x] Crear la carpeta del proyecto
  [x] Crear el repositorio Git

  [ ] Instalar Node.js
  [ ] Crear el proyecto Astro
  [ ] Instalar Symfony
  [ ] Instalar Tailwind
  [ ] Configurar MySQL
  [ ] Probar el acceso desde otra PC
```

Notas: no se inventaron secciones (la primera parte queda como texto bajo
el título), la duda sobre React se marca con `?` y no con `→`, y no se
agregó información (Node.js no se declara "no instalado" porque el
original no lo dice).
