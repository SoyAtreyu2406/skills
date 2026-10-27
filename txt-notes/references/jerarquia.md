# JERARQUÍA Y ORGANIZACIÓN DEL CONTENIDO (detalle del Paso 1)

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
