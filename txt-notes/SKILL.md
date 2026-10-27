---
name: txt-notes
description: Reescribe, organiza y formatea anotaciones personales en texto plano (.txt). Mejora claridad y redacción, agrupa conceptos relacionados y aplica una gramática visual consistente, compacta y jerárquica, preservando siempre la información y los datos técnicos. Usar cuando el usuario pegue o indique un texto o archivo de notas y pida ordenarlo, corregirlo, jerarquizarlo o darle formato, o mencione txt-notes.
---

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

## ENTRADA Y SALIDA

Al terminar, si la skill agregó contenido que no estaba en la nota
(respuestas, definiciones) o consolidó información, añadir fuera de la
nota, después del bloque, una única línea de resumen, por ejemplo:
`Agregué: 2 respuestas, 1 definición. Consolidé: 1 tarea duplicada.`
Si no hubo nada de eso, no escribir la línea.

- Texto pegado en el chat: devolver el resultado como texto plano
  dentro de un único bloque, sin comentarios intercalados.
- Archivo: no sobrescribir el original sin que el usuario lo pida.
  Por defecto crear `<nombre>_formateado.txt` junto al original.
- Si el texto ya está formateado con esta gramática, reaplicar las
  reglas sin duplicar símbolos ni estructura.
- Idioma: el mismo de la nota. Mantener el voseo o el tuteo originales.

## NOTAS AMBIGUAS O INCOMPLETAS

Las notas suelen ser telegráficas, con abreviaturas o ideas a medias.

- Expandir una abreviatura solo si el contexto la hace inequívoca; si
  no, dejarla tal cual.
- No completar frases cortadas ni adivinar el referente de un
  pronombre.
- Si algo es ilegible o ambiguo y no se puede resolver, conservarlo
  literal y marcarlo con `? [no claro: texto original]`.
- Ante contradicciones que se consolidan (ver CONSOLIDACIÓN), avisar en
  una línea final fuera de la nota: `Consolidé: X reemplaza a Y`.

## TIPO DE NOTA

Detectar el tipo de contenido (reunión, tareas, apuntes de estudio,
bitácora técnica, ideas sueltas) solo para decidir el énfasis, nunca
para inventar secciones ni nombres de plantilla.

- Reunión: destacar decisiones (`★`) y pendientes (`[ ]`) si el texto
  los expresa.
- Apuntes de estudio: mantener juntas definición y ejemplo.
- Bitácora o registro: conservar el orden cronológico.
- Texto corto o sin estructura natural: texto libre bajo el título, sin
  secciones.
- Texto largo: dividir solo cuando haya temas realmente independientes.

Fechas: conservarlas como aparecen; no inventarlas ni convertirlas si
eso agrega ambigüedad.

Datos del tipo "clave: valor" o comparaciones: pueden alinearse en una
lista o tabla ASCII solo si el original ya tiene esa forma.

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

Única excepción: las respuestas a preguntas sin respuesta y las
definiciones de términos que el usuario marcó como dudosos (ver
"RESPUESTAS A PREGUNTAS" en la gramática visual). Esa información
agregada siempre se marca como tal y nunca reemplaza ni altera lo que
el usuario escribió.

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

Ver `references/jerarquia.md` y seguir sus reglas.

Resumen: leer todo, determinar la jerarquía por relación conceptual (no por el orden original), usar la mínima estructura necesaria, no inventar nombres de sección, espaciado: 0 renglones dentro de un bloque, 1 entre bloques, 2 entre secciones `▌`. El Paso 2 no modifica lo decidido aquí.

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
★    decisión tomada
~    suposición / dato no confirmado
!    información importante
?    pregunta / investigación
$    comando ejecutable
>    salida de comando
🔗   URL independiente
-    elemento informativo de una lista
```

No introducir otros emojis o símbolos decorativos.

El símbolo debe aportar significado.

## DECISIONES `★`

`★` marca una decisión ya tomada, expresada como tal en la nota
("decidí usar Astro", "vamos con MySQL", "queda definido que...").

```text
★ Usar Astro para el frontend.
```

- No marcar como decisión una intención, idea o posibilidad ("podría
  usar", "estoy pensando en", "sería con"): eso es `→` o `~`.
- Una decisión que luego se revierte en la nota se consolida con la más
  reciente; no mantener ambas.
- Una decisión no es una tarea: si además implica algo por hacer, la
  tarea va aparte con `[ ]`.

## SUPOSICIONES `~`

`~` marca una afirmación que el usuario expresa como no confirmada
("creo que", "capaz", "quizás", "supongo", "me parece que").

```text
~ Creo que el puerto es el 3306.
```

- La reescritura nunca debe endurecer una suposición en un hecho ni
  quitarle el matiz original.
- No usar `~` para dudas formuladas como pregunta (esas son `?`), ni
  para cada frase con tono cauteloso: solo cuando la afirmación misma es
  incierta y importa distinguirla de los hechos.
- Si la suposición ya está dentro de un párrafo que explica el contexto,
  dejarla en el texto con su matiz y no extraerla.

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
- Las líneas internas de salidas (`>`) conservan su indentación
  original; solo se agrega el nivel externo del bloque y el prefijo del
  marcador.
- El código y las sentencias agrupadas (scripts, procedimientos,
  transacciones) NO reciben indentación externa: se conservan como una
  unidad inmutable, alineados a columna 0 respecto de su contenido
  interno (ver "EXCEPCIONES DE INDENTACIÓN").

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

## EXCEPCIONES DE INDENTACIÓN, BLOQUES, CÓDIGO, CONFIGURACIÓN, ÁRBOLES Y TABLAS

Ver `references/bloques-tecnicos.md` y seguir sus reglas.

Resumen: los bloques técnicos se conservan literalmente. El código (scripts, funciones, sentencias agrupadas) va a columna 0, sin cercas ni indentación externa. Configuración, árboles, salidas y comandos reciben un nivel externo de indentación sin alterar su interior. Las tablas ASCII no se convierten en listas.

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
oraciones puramente informativas. Excepción: `→ Respuesta:` bajo una
pregunta (ver "RESPUESTAS A PREGUNTAS").

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

## RESPUESTAS A PREGUNTAS

Ver `references/respuestas.md` y seguir sus reglas.

Resumen: responder las preguntas conceptuales o técnicas sin respuesta con `→ Respuesta:` bajo la pregunta; definir con `→ Definición:` los términos que el usuario marcó como dudosos; las comparaciones llevan ventajas y desventajas; las respuestas de búsqueda web citan la fuente con `🔗`; no responder las preguntas personales ni las verificaciones.

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

### Comandos sueltos vs. bloques de código

El `$` se reserva para un **comando único y ejecutable de una sola
sentencia** (una línea de shell, un TRUNCATE, un UPDATE, etc.).

No usar `$` para marcar un **bloque de código computable esencialmente
como una unidad**: un script SQL, un script de shell, un procedimiento,
una transacción (`START TRANSACTION ... COMMIT`), un bloque envuelto en
llaves, una función o cualquier agrupación donde varias líneas dependen
entre sí y deben entenderse (y ejecutarse) juntas.

Para detectarlo, preguntarse:

```text
¿Estas líneas funcionan/leen/se ejecutan como una sola entidad
(una transacción, un script, un procedimiento), o son comandos
independientes que se ejecutan por separado?
```

- Si funcionan como una unidad → bloque de código: NO anteponer `$` a
  cada línea. El código queda literal, preservado como unidad inmutable a
  columna 0 y sin símbolos en su interior.
- Si son comandos sueltos e independientes entre sí → cada uno con `$`.

Rebasar bloques que ya delimitan una unidad.

No convertir un `START TRANSACTION ... COMMIT` en varias líneas `$`
aunque en el original cada sentencia apareciera en una línea propia.

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

Ver `references/urls.md` y seguir sus reglas.

Resumen: las URLs se conservan exactamente; una URL independiente lleva `🔗`; dentro de oraciones, comandos, salidas, código o configuración permanece en su contexto; si viene en Markdown, se deshace a texto plano.

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
* ¿No se agregó información, salvo respuestas marcadas a preguntas?
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
* ¿Las decisiones tomadas utilizan `★` y no se marcaron como decisión
  simples ideas o posibilidades?
* ¿Las suposiciones explícitas utilizan `~` y no se endurecieron como
  hechos?
* ¿La línea final "Agregué/Consolidé" refleja lo que realmente se
  agregó o consolidó?
* ¿Las preguntas utilizan `?`?
* ¿Cada pregunta conceptual sin respuesta tiene una respuesta con
  `→ Respuesta:`, y las preguntas personales o de verificación se dejaron
  sin responder?
* ¿La información agregada está únicamente en respuestas marcadas y no
  se mezcló con el texto del usuario?
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
* ¿El contenido interno de los bloques no fue modificado (indentación,
  espacios, saltos de línea, comillas)?
* ¿Los bloques de configuración conservan sus valores?
* ¿No se modificaron rutas o nombres de archivos?
* ¿No se modificaron comandos?
* ¿Los bloques que son una unidad (scripts, transacciones, procedimientos)
  NO llevan `$` en cada línea y quedan como texto literal, sin cercas?
* ¿El `$` solo marca comandos sueltos e independientes, y no líneas
  individuales de un mismo bloque?
* ¿Los bloques de código se entregan sin indentación externa, preservados
  como unidad inmutable a columna 0 (no se les agregaron 2 espacios que
  alteren el contenido)?

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