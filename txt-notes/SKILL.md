---

name: txt-notes
description: Reescribe, organiza y formatea anotaciones personales en texto plano (.txt). Mejora claridad y redacción, agrupa conceptos relacionados y aplica una gramática visual consistente, compacta y jerárquica, preservando siempre la información y los datos técnicos.
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# TXT-NOTES

## OBJETIVO

Transformar anotaciones en texto claro, ordenado y fácil de consultar.

El proceso se ejecuta en dos pasos:

```text
anotaciones originales
        ↓
┌─────────────────────────────┐
│ PASO 1                      │
│ reescritura + organización  │
│ conceptual                  │
└─────────────────────────────┘
        ↓
┌─────────────────────────────┐
│ PASO 2                      │
│ formato visual               │
└─────────────────────────────┘
```

Los dos pasos se resuelven internamente, uno a continuación del otro, y
se entrega un único resultado final ya formateado. No se muestra al
usuario una salida intermedia entre el paso 1 y el paso 2.

## REGLA PRINCIPAL

Paso 1: comprender, reescribir y organizar conceptualmente el contenido,
sin aplicar todavía la gramática visual.
Paso 2: aplicar el formato visual sobre el resultado del paso 1.

Nunca modificar el contenido solamente para conseguir una estructura visual.
La reescritura mejora el texto; el formato lo presenta. La información no cambia.

La skill no debe intentar que todo tenga un encabezado. Una buena salida
puede perfectamente ser texto libre bajo el título principal sin
secciones, siempre que el contenido lo permita.

---

# PASO 1 · REESCRITURA Y ORGANIZACIÓN

Este paso comprende, reescribe y jerarquiza el contenido conceptualmente.
No se aplica todavía ningún símbolo de la gramática visual: eso ocurre
recién en el Paso 2.

## REESCRITURA

Reescribir el contenido para mejorar:

- claridad;
- gramática;
- redacción;
- orden de las ideas;
- eliminación de repeticiones innecesarias.

Preservar siempre:

- toda la información;
- el significado;
- la intención;
- los datos técnicos;
- los comandos;
- las URLs;
- los nombres;
- las versiones;
- las rutas;
- los valores;
- los ejemplos;
- el registro y el tono de la nota.

No agregar información que no esté presente en las anotaciones.

## QUÉ SÍ PUEDE HACER LA REESCRITURA

- reformular oraciones confusas o ambiguas sin cambiar su significado;
- dividir o unir frases para mejorar la fluidez;
- eliminar redundancias que no aportan información;
- corregir errores gramaticales y ortográficos;
- unificar tiempos verbales cuando el significado no cambie;
- reordenar las ideas dentro de un mismo bloque cuando el orden original confunda;
- convertir enumeraciones dentro de una oración en listas cuando eso mejore la lectura.

## QUÉ NO DEBE HACER LA REESCRITURA

- modificar vocabulario técnico ni términos propios del dominio;
- fusionar hechos, condiciones o limitaciones distintas en un único enunciado;
- acortar a tal punto que se pierda contexto o matices;
- generalizar ejemplos, valores o detalles concretos;
- agregar, inferir o inventar información;
- traducir contenido;
- presentar una suposición como si fuera un hecho;
- cambiar el registro de la nota (primera persona, tono personal o casual);
- reescribir bloques técnicos: código, configuración, comandos, salidas,
  árboles y tablas se conservan literalmente.

## VERIFICACIÓN DESPUÉS DE REESCRIBIR

Antes de continuar con la organización, comprobar:

```text
¿Cambió el significado de alguna afirmación?
        ↓
¿Se perdió algún dato?
        ↓
¿Se agregó algo que no estaba?
        ↓
¿Los fragmentos reescritos siguen sonando como la misma persona?
        ↓
¿Los datos técnicos quedaron idénticos?
```

Si alguna respuesta es afirmativa para pérdida o agregado, corregir antes de seguir.

## CONSOLIDACIÓN DE INFORMACIÓN

Cuando varias anotaciones expresen la misma información, consolidarlas
en una única formulación clara.

Si una anotación posterior actualiza, corrige o contradice una anotación
anterior, conservar la información más reciente y evitar mantener ambas
como si fueran simultáneamente válidas.

No duplicar una misma tarea, decisión, dato o afirmación en diferentes
partes del documento.

Ejemplo:

  todavía no hice el repo de git

  ya hice la carpeta y git

El resultado debe reflejar el estado más reciente:

  [x] Crear la carpeta
  [x] Crear el repositorio de Git

El objetivo es transformar un conjunto de notas acumulativas en un
documento coherente, no simplemente acomodar cada frase.

---

## ORGANIZACIÓN, JERARQUÍA Y ESTRUCTURACIÓN DEL CONTENIDO

Antes de aplicar cualquier formato visual, procesar el texto siguiendo
las reglas de esta sección.

El objetivo es transformar un texto desordenado en un contenido
**organizado, categorizado, jerárquico, coherente y fácil de leer**, sin
alterar su significado ni perder información.

Esta etapa establece la jerarquía y el orden lógico. El formato final se
aplica después y no debe modificarlos.

### 1 · ANALIZAR TODO EL CONTENIDO

Primero leer y analizar el texto completo.

Identificar:

- tema principal;
- secciones principales;
- subsecciones;
- subapartados;
- bloques de contenido;
- listas;
- procedimientos;
- explicaciones;
- datos;
- consideraciones importantes;
- problemas;
- próximos pasos.

No tomar el orden original como definitivo.

### 2 · DETERMINAR LA JERARQUÍA

La jerarquía debe determinarse según la **relación conceptual entre los
contenidos**, no únicamente según cómo aparecen escritos originalmente.

No todos los títulos o encabezados tienen el mismo nivel.

Utilizar una jerarquía lógica:

### Nivel 1 — Sección principal `▌`

Representa un tema amplio e independiente dentro del documento.

```text
PROYECTO WEB

FUNCIONALIDADES

CONFIGURACIÓN
```

Cada uno representa una sección principal diferente. Cuando se pasa de
una sección principal a otra, corresponde una separación de 2 renglones
vacíos.

### Nivel 2 — Subsección `▪`

Representa un tema específico que pertenece directamente a una sección
principal.

```text
PROYECTO WEB

Tecnologías utilizadas:
...

Frontend:
...

Backend:
...

API:
...
```

Si `Frontend`, `Backend` y `API` forman parte del contenido de
`PROYECTO WEB`, no deben tratarse como secciones principales
independientes sino como subsecciones. Entre subsecciones de una misma
sección corresponde 1 renglón vacío.

### Nivel 3 — Subapartado

Representa un aspecto específico dentro de una subsección.

```text
Frontend:
El frontend está desarrollado con Astro.

Componentes:
Header
Footer
Cards
Formularios
```

En este caso, `Componentes` pertenece a `Frontend` y no debe elevarse al
mismo nivel que `Frontend`. En la gramática visual el subapartado no tiene
un símbolo propio: se expresa como contenido (párrafo, lista o bloque)
dentro de la subsección `▪` a la que pertenece.

### Nivel 4 — Contenido

Es la información que desarrolla, explica o completa el encabezado
anterior.

Puede ser:

- un párrafo;
- una lista;
- una serie de datos;
- un procedimiento;
- un conjunto de valores;
- una explicación.

El contenido no debe convertirse en una nueva sección simplemente porque
aparezca en una línea independiente.

### 3 · REGLA PARA DETERMINAR EL NIVEL

Antes de asignar un nivel a un título o encabezado, preguntarse:

**“¿Este concepto contiene al anterior, pertenece al anterior o
representa un tema independiente?”**

- Si representa un tema independiente → Sección principal `▌`.
- Si desarrolla un tema dentro de una sección → Subsección `▪`.
- Si desarrolla un aspecto dentro de una subsección → Subapartado (contenido).
- Si simplemente explica o enumera el concepto anterior → Contenido.

No elevar un elemento de jerarquía solamente porque esté escrito con
mayúsculas, tenga `:` o esté separado por renglones.

La jerarquía debe surgir del **significado y la relación entre los
conceptos**.

### 4 · EJEMPLO DE JERARQUÍA CORRECTA

Dado este contenido:

```text
PROYECTO WEB

Tecnologías utilizadas:
Astro
Symfony
MySQL

Frontend:
El frontend está desarrollado con Astro.

Componentes:
Header
Footer
Cards
Formularios

Backend:
Symfony se utiliza para manejar la lógica.

API:
La API permite obtener productos, usuarios y pedidos.

Endpoints principales:
GET /productos
GET /usuarios
POST /pedidos


FUNCIONALIDADES

Usuarios:
El sistema permite registrar nuevos usuarios.

Productos:
Se pueden crear, editar y eliminar productos.

Pedidos:
El usuario puede realizar un pedido.
```

La estructura conceptual debe interpretarse como:

```text
PROYECTO WEB
├── Tecnologías utilizadas
├── Frontend
│   └── Componentes
├── Backend
└── API
    └── Endpoints principales

FUNCIONALIDADES
├── Usuarios
├── Productos
└── Pedidos
```

No significa que deban mostrarse esos símbolos en el resultado final. Es
únicamente la estructura conceptual que debe utilizarse para organizar el
contenido.

### 5 · NO CREAR JERARQUÍAS ARTIFICIALES

No crear niveles solamente para que el documento parezca más estructurado.
La organización debe surgir del contenido original y de las relaciones
entre sus elementos.

Si dos elementos tienen realmente la misma importancia y pertenecen al
mismo nivel conceptual, mantenerlos en el mismo nivel.

Si un elemento depende conceptualmente de otro, colocarlo debajo de ese
elemento.

No convertir automáticamente cada línea terminada en `:` en una sección.

Por ejemplo:

```text
Estados del pedido:
Pendiente
Confirmado
Enviado
Entregado
```

`Estados del pedido` es el encabezado del bloque y los elementos
siguientes son su contenido. No debe convertirse en:

```text
Estados del pedido:

Pendiente

Confirmado

Enviado

Entregado
```

No crear una sección o subsección solamente para darle un lugar a un
conjunto de elementos. Si un contenido puede quedar correctamente como
párrafo, lista, bloque técnico, tarea, pregunta o idea dentro de la
estructura existente, no crear una nueva estructura para contenerlo.

No utilizar encabezados como contenedores genéricos para información que
no necesita una división propia. Priorizar una estructura simple y
natural sobre una estructura exhaustivamente categorizada.

Ante la duda, la skill debe preguntarse:

  ¿Este contenido realmente necesita un nuevo nivel jerárquico?

Si la respuesta es no, mantenerlo en el nivel actual.

### 6 · AGRUPAR Y REUBICAR

Si una subsección aparece separada de la sección a la que pertenece,
reubicarla junto con su contenido relacionado.

Si un subapartado aparece antes que su tema principal, reorganizar el
contenido para recuperar la jerarquía correcta.

Ejemplo:

```text
Componentes:
Header
Footer

...

Frontend:
El frontend utiliza Astro.
```

Debe reorganizarse conceptualmente como:

```text
Frontend:
El frontend utiliza Astro.

Componentes:
Header
Footer
```

No mantener un bloque separado únicamente porque así estaba en el texto
original.

### 7 · TÍTULOS Y NOMBRES DE SECCIÓN

Utilizar `▌` cuando:

1. el texto de las anotaciones contenga de forma explícita un título o
   encabezado (por ejemplo `Pendiente:`, `CONFIGURACIÓN`); o
2. el contenido presente un bloque temático claramente delimitado, cuyo
   nombre surja directamente de lo que el texto dice.

En el primer caso, normalizar la presentación visual pero conservar el
texto del título siempre que sea posible. No reemplazar un encabezado
existente por un sinónimo, resumen o categoría inventada.

```text
Pendiente:
```

puede convertirse en:

```text
▌ PENDIENTE
```

pero no debe reemplazarse por un nombre genérico que no esté en el texto.

No utilizar nombres de plantilla para clasificar contenido que no las
sugiere por sí mismo:

- Introducción;
- Objetivo;
- Conclusión;
- Resumen;
- Notas;
- Recursos;
- Referencias;
- Próximos pasos.

Por ejemplo, si el texto dice:

```text
Creo que primero debería comprobar la conexión local, después probar el
acceso desde otro dispositivo y recién después configurar la base de datos.
```

no crear:

```text
▌ PRÓXIMOS PASOS
```

No crear una sección para cada párrafo, oración, ejemplo o condición.
Si para crear `▌` hay que resumir, interpretar o inventar el nombre de
una categoría, no utilizar `▌`: mantener el contenido como texto normal.

### 8 · REGLAS DE ESPACIADO SEGÚN LA JERARQUÍA

El espaciado debe reflejar la jerarquía.

### Después de `:`

No dejar ningún renglón vacío cuando `:` introduce contenido directamente
relacionado.

```text
Tecnologías utilizadas:
Astro
Symfony
MySQL
```

### Entre bloques de una misma sección

Dejar 1 renglón vacío.

```text
Frontend:
El frontend está desarrollado con Astro.

Backend:
Symfony maneja la lógica del sistema.
```

### Entre secciones principales

Dejar 2 renglones vacíos.

```text
Backend:
Symfony maneja la lógica del sistema.


FUNCIONALIDADES

Usuarios:
El sistema permite registrar usuarios.
```

### Dentro del mismo bloque

No dejar renglones vacíos.

```text
Endpoints principales:
GET /productos
GET /usuarios
POST /pedidos
```

### 9 · LOS RENGLONES ORIGINALES SON UNA REFERENCIA, NO UNA REGLA

Los renglones vacíos originales pueden indicar una intención de
separación, pero no deben conservarse automáticamente.

Interpretar su función.

Si la separación original no coincide con la jerarquía real del
contenido, corregirla.

El resultado debe tener un espaciado **consistente y determinado por la
estructura**.

### 10 · ORDEN DE PROCESAMIENTO

Seguir siempre este orden:

1. Leer todo el texto.
2. Identificar los temas principales.
3. Identificar relaciones entre los contenidos.
4. Determinar la jerarquía.
5. Agrupar información relacionada.
6. Reubicar contenido cuando sea necesario.
7. Separar secciones, subsecciones y subapartados.
8. Limpiar repeticiones y separaciones incorrectas.
9. Aplicar las reglas de espaciado según la jerarquía.
10. Generar la estructura organizada.

Con esto finaliza el Paso 1. Recién después continuar con el Paso 2 y
aplicar el formato final definido por la skill.

**La jerarquía conceptual debe establecerse antes de aplicar cualquier
formato visual.**

El Paso 2 no debe modificar la jerarquía, agrupación ni orden lógico
determinados en el Paso 1.

---

# PASO 2 · FORMATO

Una vez resuelto el Paso 1 (contenido reescrito y organizado
conceptualmente, sin símbolos), aplicar la gramática visual definida en
esta skill sobre ese resultado.

## GRAMÁTICA VISUAL

Utilizar únicamente los siguientes elementos:

```text
◆    título principal
▌    sección principal
▪    subsección conceptual real
[ ]  tarea pendiente
[x]  tarea completada
◐    tarea en progreso
→    idea / acción / relación / consecuencia / aclaración
!    información importante
?    pregunta / investigación
$    comando ejecutable
>    salida de comando
🔗   URL independiente
-    elemento informativo de una lista
```

No introducir otros emojis o símbolos decorativos.

El símbolo debe aportar significado.

## TÍTULO PRINCIPAL

El título principal utiliza:

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  TÍTULO PRINCIPAL · FECHA
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

La fecha solo debe aparecer si existe en el contenido o si forma parte
evidente del título original. No inventar fechas.

No utilizar este formato para títulos secundarios. Solo el título
principal puede utilizar esta línea decorativa.

## SECCIONES PRINCIPALES

Las secciones principales utilizan:

```text
▌ NOMBRE DE SECCIÓN
```

No utilizar dos puntos al final del nombre.

```text
▌ CONFIGURACIÓN
```

No:

```text
▌ CONFIGURACIÓN:
```

No agregar líneas decorativas debajo de las secciones.

## INDENTACIÓN

Cada nivel jerárquico se indentiza con 2 espacios.

```text
Nivel 0 → sin indentación (◆, ▌ y texto fuera de secciones)
Nivel 1 → 2 espacios (contenido y elementos bajo ▌)
Nivel 2 → 4 espacios (contenido bajo ▪ y bloques introducidos)
Nivel 3 → 6 espacios (bloques introducidos dentro de ▪)
```

Reglas:

- El texto y los elementos directos (`-`, `[ ]`, `$`, `>`, `🔗`) que
  pertenecen a una sección `▌` se indentizan con 2 espacios.
- Una subsección `▪` se indentiza con 2 espacios; su contenido se
  indentiza con 4 espacios.
- Un bloque (`$`, `>`, `🔗`, `-`) que sigue a una frase introductoria se
  indentiza un nivel más que la frase que lo introduce. Este anidamiento
  se repite recursivamente: cada nivel adicional suma 2 espacios.
- Las descripciones con `→` se indentizan bajo el comando o el elemento
  al que describen.
- El contenido fuera de cualquier sección va sin indentación.
- Los bloques introducidos por una frase terminada en `:` se indentizan
  un nivel respecto de esa frase.
- Las líneas internas de salidas (`>`), código, configuración y árboles
  conservan su indentación original; solo se agrega el nivel externo del
  bloque y el prefijo del marcador.

Ejemplo:

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  TÍTULO PRINCIPAL
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

▌ SECCIÓN 1

  Texto de la sección.

  - elemento
  - elemento

  Para ejecutar:

    $ comando

  Ejemplo:

    > línea de salida
    >    línea con indentación original

  Salida de comando:

    $ ipconfig /all
      → Muestra información detallada.


▌ SECCIÓN 2

  ▪ Subsección

    Texto de la subsección.

    Si ejecutás:

      $ comando
```

La indentación debe ser consistente en todo el documento: el mismo tipo
de contenido debe utilizar siempre los mismos espacios.

## EXCEPCIONES DE INDENTACIÓN

La indentación estructural de la skill organiza la **nota**, pero nunca
debe modificar la indentación interna del contenido técnico original.

La skill debe distinguir entre:

```text
indentación estructural de la nota (2 espacios por nivel jerárquico)
indentación que pertenece al contenido original (se preserva tal cual)
```

Preservar exactamente la indentación original de:

- código fuente;
- árboles de directorios;
- archivos de configuración;
- variables de entorno;
- JSON;
- YAML;
- XML;
- SQL;
- comandos multilínea;
- salidas de comandos;
- ejemplos técnicos cuya indentación tenga significado.

La indentación estructural solo agrega un nivel externo uniforme cuando
una frase introduce el bloque mediante `:`; nunca modifica la
indentación interna de cada línea.

Ejemplo:

```text
El código que estoy probando es:

  function sumar(a, b) {
  const resultado = a + b;
  return resultado;
  }

  console.log(sumar(10, 20));
```

Si el contenido técnico ya posee indentación propia, conservarla
exactamente como aparece en el original: solo se agrega el nivel externo
que introduce el `:`, sin re-indentar las líneas internas.

## BLOQUES INTRODUCIDOS POR DOS PUNTOS

Cuando una frase introduce un bloque mediante `:`, el bloque siguiente
debe indentarse un nivel respecto del texto que lo introduce.

Esto aplica a:

```text
El proyecto tiene esta estructura:

  project/
  ├── public/
  └── src/
```

```text
La configuración es:

  APP_ENV=dev
  APP_URL=http://localhost:4321
```

```text
Por ejemplo:

  > Adaptador de LAN inalámbrica Wi-Fi:
  >    Dirección IPv4 : 192.168.1.105
```

Y también:

```text
Para ejecutar el proyecto:

  $ npm install
  $ npm run dev
```

Pero la indentación interna del bloque se conserva.

Por ejemplo, el árbol original:

```text
project/
├── src/
│   └── pages/
│       └── index.astro
```

se transforma visualmente en:

```text
  project/
  ├── src/
  │   └── pages/
  │       └── index.astro
```

No se modifica su estructura; simplemente se agrega un nivel externo de
indentación.

## LISTAS INFORMATIVAS

Las listas informativas utilizan:

```text
- elemento
- elemento
- elemento
```

```text
▌ ADAPTADORES

  - Ethernet
  - Wi-Fi
  - Bluetooth
  - Hyper-V
  - WSL
```

No utilizar `▪` para cada elemento.

No utilizar `[ ]` si el elemento no representa una tarea.

## TAREAS

Las tareas pendientes utilizan:

```text
[ ] tarea pendiente
```

Las tareas completadas:

```text
[x] tarea completada
```

Las tareas en progreso:

```text
◐ tarea en progreso
```

```text
▌ PENDIENTE

  [ ] Configurar Docker
  [ ] Probar conexión
  [x] Crear base de datos
  ◐ Implementar sincronización
```

No transformar una frase informativa en una tarea si originalmente no
representa una acción pendiente.

No convertir automáticamente ideas, dudas, decisiones, restricciones,
planes o posibilidades en tareas `[ ]`.

Usar `[ ]` solamente cuando el contenido expresa claramente una tarea
pendiente o algo que debe realizarse.

Una pregunta debe permanecer como `?`.
Una idea debe permanecer como `→`.
Una advertencia debe permanecer como `!`.
Una restricción debe permanecer como texto normal, salvo que el contexto
la identifique claramente como una advertencia.

## IDEAS Y ACCIONES

Utilizar `→` para representar:

- ideas;
- acciones;
- relaciones;
- consecuencias;
- aclaraciones breves;
- conclusiones prácticas.

```text
→ Usar la IP del adaptador Wi-Fi.
→ Probar primero desde otro dispositivo de la misma red.
```

No convertir automáticamente cada oración en `→`. El símbolo debe
utilizarse cuando aporta significado.

No usar `→` para restricciones, advertencias, planes futuros, dudas ni
oraciones puramente informativas.

`→` se reserva para cuando la oración original expresa explícitamente
una idea, una propuesta de acción, una relación, una consecuencia o una
aclaración independiente.

## NO MARCAR ORACIONES INTRODUCTORIAS

No aplicar un marcador semántico (`→`, `!`, `?`, `$`, `>` o `🔗`) a una
oración solamente porque introduce o precede contenido que pertenece a
esa categoría.

Una oración que conduce hacia un comando, una salida, una URL o una
advertencia debe permanecer como texto normal.

Correcto:

```text
Para probarlo desde otro dispositivo puedo usar:

  🔗 http://192.168.1.105:4321
```

Incorrecto:

```text
→ Para probarlo desde otro dispositivo puedo usar:

  🔗 http://192.168.1.105:4321
```

Del mismo modo:

```text
Para empezar necesito instalar las dependencias y levantar el proyecto
localmente.

$ npm install
$ npm run dev
```

no debe convertirse en:

```text
→ Para empezar necesito instalar las dependencias y levantar el proyecto
  localmente.

$ npm install
$ npm run dev
```

El marcador se reserva para la oración que en sí misma expresa una idea,
acción, advertencia o pregunta independiente, no para la que introduce
contenido posterior.

Ejemplo válido (la oración expresa por sí misma una propuesta de acción):

```text
→ Creo que primero debería comprobar la conexión local, después probar el
  acceso desde otro dispositivo y recién después configurar la base de datos.
```

## INFORMACIÓN IMPORTANTE

Utilizar `!` únicamente cuando la información sea explícitamente
importante o crítica.

```text
! No modificar este valor.
```

No utilizar `!` decorativamente.
No convertir toda información técnica en información importante.

`!` debe aplicarse a la unidad completa que realmente constituye la
advertencia o la información importante. No extender el marcador a todo
el contenido que aparece después de una frase importante.

```text
! No subir credenciales al repositorio.

El archivo de configuración tiene actualmente:

  APP_ENV=dev
  APP_URL=http://localhost:4321
```

es preferible a:

```text
! No subir credenciales al repositorio. El archivo de configuración
  tiene actualmente:

  APP_ENV=dev
  APP_URL=http://localhost:4321
```

## PREGUNTAS

Utilizar `?` para preguntas o cuestiones que requieren investigación.

```text
? ¿Conviene utilizar SSR?
? ¿Conviene usar Docker?
? Verificar el puerto utilizado por la balanza.
```

No convertir una frase interrogativa que forma parte de una explicación
en una tarea automáticamente.

## COMANDOS

Los comandos ejecutables utilizan:

```text
$ comando
```

```text
$ ipconfig
```

Mantener el comando exactamente como aparece. No cambiar argumentos,
parámetros, mayúsculas, minúsculas, rutas, variables, valores u opciones.

## SALIDA DE COMANDOS

La salida de comandos utiliza:

```text
> salida
```

```text
> Adaptador de LAN inalámbrica Wi-Fi:
>    Dirección IPv4 : 192.168.1.105
```

La salida debe conservar su contenido original.

No interpretar una línea de salida como texto normal solamente porque
contenga una palabra que parezca un título.

## URLs

### Preservación exacta

Las URLs deben conservarse exactamente como aparecen en el contenido
original. Nunca:

- agregar `http://`;
- agregar `https://`;
- eliminar `http://`;
- eliminar `https://`;
- agregar `www.`;
- eliminar `www.`;
- cambiar `www.` por otra forma;
- cambiar el dominio;
- cambiar el puerto;
- cambiar la ruta;
- cambiar parámetros;
- corregir una URL;
- normalizar una URL;
- cambiar mayúsculas o minúsculas;
- modificar cualquier otra parte de la URL.

La única modificación permitida es agregar el marcador visual `🔗`
cuando la URL sea un elemento independiente.

### No convertir URLs a markdown

Nunca convertir una URL a formato Markdown, HTML u otro formato de enlace.

Si el contenido original contiene `www.google.com`, conservarla como
`www.google.com` y no convertirla en `[www.google.com](http://www.google.com)`.

### URL que ya viene en formato markdown

Si el contenido original contiene una URL en sintaxis Markdown, por
ejemplo `[www.google.com](http://www.google.com)`, deshacer el formato
Markdown y conservar la URL en texto plano:

```text
www.google.com
```

El contenido de la URL se conserva exactamente; solo se elimina la
sintaxis de enlace. La URL resultante se trata según el contexto:

- si era un elemento independiente, se marca con `🔗`;
- si formaba parte de una oración, permanece dentro de esa oración.

### URLs independientes

Una URL independiente utiliza:

```text
🔗 URL
```

```text
🔗 https://example.com
🔗 http://localhost:4321
🔗 www.google.com
```

Nunca:

```text
🔗 http://www.google.com
```

### URL dentro de una explicación

Si una URL forma parte de una oración o explicación, debe permanecer
dentro de esa oración.

```text
Para acceder al proyecto podés usar http://localhost:4321 desde el navegador.
```

No convertirla en una URL independiente.

### URL dentro de un comando

```text
$ curl https://example.com/api/products
```

No convertirla en:

```text
$ curl
🔗 https://example.com/api/products
```

### URL dentro de una salida

```text
> Local: http://localhost:4321/
```

No convertirla en una URL independiente.

### URL dentro de código o configuración

```text
const url = "https://example.com";
```

```text
API_URL=https://example.com/api
```

La URL forma parte del bloque y permanece exactamente en su interior.

### Regla de contexto para URLs

```text
URL independiente
        ↓
🔗 URL

URL dentro de comando
        ↓
$ comando URL

URL dentro de salida
        ↓
> salida URL

URL dentro de código/configuración
        ↓
preservar dentro del bloque
```

La clasificación puede cambiar. El contenido de la URL, nunca.

## CÓDIGO

Los bloques de código deben conservar:

- sintaxis;
- indentación significativa;
- variables;
- nombres;
- valores;
- comentarios;
- URLs;
- comandos;
- rutas;
- nombres de archivos;
- estructuras.

No embellecer código.
No corregir código.
No traducir código.
No agregar símbolos de la gramática visual dentro del código.

Todo bloque de código debe delimitarse con cercas ``` (sin indicar
lenguaje, salvo que el original ya lo especifique), para diferenciarlo
visualmente del resto del texto.

```text
const url = "https://example.com";
const port = 3000;
```

debe permanecer exactamente así, envuelto en las cercas.

## CONFIGURACIÓN

Los bloques de configuración deben preservarse literalmente. Esto
incluye `.env`, YAML, JSON, XML, INI, variables de entorno, comandos y
parámetros. No cambiar valores.

```text
APP_ENV=dev
APP_URL=http://localhost:8000
DATABASE_PORT=5432
```

No modificar las URLs ni los valores.

## ÁRBOLES Y ESTRUCTURAS

Los árboles de directorios y estructuras ASCII deben conservar su
estructura.

```text
src/
├── Command/
│   └── UpdateProductsCommand.php
├── Entity/
│   └── Producto.php
└── Service/
    └── TicketService.php
```

No reemplazar caracteres del árbol por `-`, `▪` u otros símbolos.
No modificar la indentación necesaria para representar la estructura.

## TABLAS

Las tablas ASCII deben conservar columnas, filas, separadores, alineación
cuando sea significativa, nombres y valores.

```text
+------------+--------+
| Producto   | Precio |
+------------+--------+
| Pan        | 100.00 |
| Torta      | 500.00 |
+------------+--------+
```

No reemplazar la tabla por una lista.
No introducir separadores decorativos adicionales.

## SEPARADORES

No utilizar líneas horizontales decorativas para separar secciones.

La única excepción es el título principal:

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  TÍTULO
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Las tablas y estructuras ASCII pueden conservar sus propios separadores
porque forman parte de su estructura.

## DENSIDAD VISUAL

El resultado debe parecer una **nota personal bien organizada**, no un
documento corporativo ni una página web.

Preferir:

```text
▌ SECCIÓN

  explicación

  - elemento
  - elemento

  explicación adicional
```

sobre una estructura excesivamente fragmentada cuando los bloques forman
parte del mismo concepto. La densidad debe ser cómoda de leer.

## ESPACIADO COMPACTO

El espaciado se determina por la jerarquía (ver "Reglas de espaciado
según la jerarquía" en ORGANIZACIÓN):

- dentro de un mismo bloque: sin renglones vacíos;
- entre bloques o elementos consecutivos de una misma sección: 1 renglón
  vacío;
- entre secciones principales `▌`: 2 renglones vacíos.

No insertar renglones vacíos entre elementos consecutivos del mismo grupo
(lista y lista, párrafo que continúa el bloque, etc.) salvo que sean
bloques conceptualmente separados.

Mantener el resultado compacto: nunca más de 2 renglones vacíos
consecutivos.

---

# VALIDACIÓN FINAL

Antes de entregar el resultado comprobar:

## Contenido y reescritura

* ¿Se conservó toda la información?
* ¿No se agregó información?
* ¿No se cambió el significado ni la intención?
* ¿Se mejoró realmente la claridad o solo se cambiaron palabras?
* ¿Los datos técnicos (comandos, URLs, versiones, rutas, valores,
  nombres) quedaron idénticos?
* ¿No se fusionaron hechos o condiciones distintos en un mismo enunciado?
* ¿No se eliminó contexto necesario?
* ¿No se usaron nombres de sección de plantilla?
* ¿La nota sigue sonando como la misma persona?
* ¿Se consolidó la información duplicada o contradictoria en una única
  formulación, reflejando el estado más reciente?

## Jerarquía

* ¿Existe un título principal con `◆` cuando corresponde?
* ¿Las secciones principales utilizan `▌`?
* ¿Las subsecciones `▪` representan realmente divisiones conceptuales
  independientes?
* ¿Se evitó convertir categorías y agrupadores simples en `▪`?
* ¿Se evitó crear una subsección para cada párrafo, ejemplo, condición o
  instrucción?
* ¿La jerarquía utilizada es la mínima necesaria?
* ¿La indentación refleja correctamente la estructura?
* ¿Se evitó forzar la estructura, creando secciones o subsecciones solo
  para darle un lugar a un conjunto de elementos?
* ¿El contenido que podría quedar como texto, lista o bloque dentro de la
  estructura existente no fue convertido en una división innecesaria? ¿O,
  al contrario, toda la nota quedó encabezada cuando no era necesario?
* ¿La jerarquía (sección, subsección, subapartado, contenido) se determinó
  por la relación conceptual entre los contenidos y no por el orden o el
  formato original?
* ¿Un subapartado no fue elevado al mismo nivel que la subsección `▪` a la
  que pertenece?
* ¿El espaciado entre bloques (1 renglón) y entre secciones principales
  `▌` (2 renglones) es consistente en todo el documento?

## Gramática visual

* ¿Las tareas utilizan `[ ]`, `[x]` o `◐`?
* ¿Las ideas y acciones utilizan `→` cuando corresponde?
* ¿Se evitó aplicar `→` a oraciones que solo introducen o preceden
  contenido posterior?
* ¿La información explícitamente importante utiliza `!`?
* ¿Las preguntas utilizan `?`?
* ¿Los comandos utilizan `$`?
* ¿Las salidas de comandos utilizan `>`?
* ¿Las URLs independientes utilizan `🔗`?
* ¿No se utilizaron emojis distintos de `🔗`?

## URLs

* ¿Las URLs conservan exactamente su contenido original?
* ¿No se agregó ni eliminó `http://`, `https://` o `www.`?
* ¿No se modificó el dominio, el puerto, la ruta ni los parámetros?
* ¿Las URLs dentro de comandos, salidas, código y configuración
  permanecen dentro de su contexto?
* ¿Se deshizo el formato Markdown cuando la URL ya venía como
  `[texto](url)`?

## Formato técnico

* ¿Las tablas conservan su estructura?
* ¿Los árboles conservan su estructura?
* ¿Los bloques de código conservan su sintaxis?
* ¿Los bloques de configuración conservan sus valores?
* ¿No se modificaron rutas o nombres de archivos?
* ¿No se modificaron comandos?

## Fragmentación

* ¿Se evitaron subsecciones innecesarias?
* ¿Se mantuvieron juntas las explicaciones relacionadas?
* ¿Los ejemplos permanecen junto al concepto que explican?
* ¿Las condiciones permanecen dentro del bloque al que pertenecen?
* ¿No se convirtió cada etiqueta en una subsección?
* ¿No se convirtió cada cambio de párrafo en una nueva jerarquía?

## Decoración

* ¿Se evitaron separadores innecesarios?
* ¿Se evitaron símbolos decorativos?
* ¿La presentación sigue pareciendo una nota `.txt`?
* ¿Cada símbolo utilizado aporta información?

---

# REGLA DE PRIORIDAD ABSOLUTA

Si dos reglas entran en conflicto, utilizar este orden:

```text
contenido e intención
        ↓
reescritura que preserve el significado
        ↓
organización conceptual justificada
        ↓
gramática visual
```

Nunca sacrificar contenido o significado para conseguir una presentación
más pulida.

El objetivo no es maximizar la cantidad de símbolos.

El objetivo es conseguir **la menor cantidad de estructura necesaria para
que la nota sea clara, ordenada y fácil de recorrer**.