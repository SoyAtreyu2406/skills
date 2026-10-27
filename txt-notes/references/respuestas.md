# RESPUESTAS A PREGUNTAS (detalle)

## RESPUESTAS A PREGUNTAS

Cuando una pregunta no tiene respuesta inmediata (ni en la misma línea
ni en las líneas siguientes), la skill debe responderla o aportar
información útil.

Cuándo responder:

- preguntas conceptuales o de definición (¿Qué es una landing?);
- preguntas factuales o técnicas (¿Qué puerto usa MySQL por defecto?);
- dudas de comparación o conveniencia (¿Conviene usar Docker?): dar los
  criterios, ventajas y desventajas relevantes, sin decidir por el
  usuario.

Cuándo NO responder:

- la nota ya contiene la respuesta, aunque esté más abajo o más arriba:
  en ese caso consolidarla junto a la pregunta;
- la pregunta depende de información personal o de contexto que solo el
  usuario tiene (¿Le pregunté a Juan?, ¿Cuándo es la reunión?): dejarla
  como `?` sin respuesta;
- es una tarea de investigación o verificación ("? Verificar el puerto
  de la balanza"): es una acción pendiente, no una duda conceptual.

Cómo presentarla:

- la pregunta conserva su `?` y su texto, sin cambios;
- la respuesta va en la línea siguiente, indentada un nivel, con `→` y
  el prefijo `Respuesta:` para distinguirla del contenido del usuario;
- breve y precisa: definición en 1 o 2 oraciones, y un ejemplo solo si
  ayuda a entenderla;
- si la respuesta necesita más de unas pocas líneas, usar una lista `-`
  bajo la respuesta.

```text
? ¿Qué es una landing?
  → Respuesta: página web de una sola pantalla pensada para que el
    visitante realice una acción concreta (suscribirse, comprar,
    registrarse).
  - Ejemplo: página de lanzamiento de un producto con un botón
    "Comprar ahora".
```

Indentación:

- la respuesta (`→ Respuesta:`, `→ Definición:`), sus listas `-` y la
  fuente `🔗` van un nivel (2 espacios) más adentro que la pregunta `?`
  a la que pertenecen, sea cual sea el nivel de la pregunta;
- las líneas que continúan una respuesta se alinean 2 espacios después
  del `→`;
- no se aplica la excepción del código: si una respuesta incluye código,
  se sigue la regla de código de `bloques-tecnicos.md`.

```text
▌ DUDAS

  ? ¿Qué es una landing?
    → Respuesta: página web de una sola pantalla pensada para que el
      visitante realice una acción concreta.
    - Ejemplo: página de lanzamiento con un botón "Comprar ahora".
```

Preguntas de comparación (¿X o Y?, ¿conviene X?):

- presentar ventajas y desventajas en dos listas paralelas bajo la
  respuesta, o en una tabla ASCII corta si hay varios criterios;
- cerrar con el criterio que inclina la balanza según el caso, sin
  decidir por el usuario.

```text
? ¿Conviene usar Docker?
  → Respuesta: depende de cuánto necesites reproducir el entorno.
  - A favor: entorno idéntico en cada máquina, fácil de recrear.
  - En contra: más consumo de recursos y una capa más para depurar.
```

Términos dudosos:

Si el usuario muestra duda sobre un término ("no sé qué es SSR", "SSR
(?)", "qué es un webhook"), agregar bajo ese texto una definición con
`→ Definición:` y, si ayuda, un ejemplo con `-`. No definir términos
que el usuario no marcó como dudosos, aunque sean técnicos.

```text
? No sé qué es SSR.
  → Definición: renderizado del lado del servidor; el HTML se genera en
    el servidor en cada pedido, en lugar de en el navegador.
```

Fuentes:

Cuando la respuesta provenga de una búsqueda web, agregar la fuente con
`🔗` en la línea final de la respuesta, conservando la URL exacta. Si la
respuesta sale del conocimiento propio, no agregar fuente.

```text
? ¿Qué puerto usa MySQL por defecto?
  → Respuesta: el 3306.
  🔗 https://dev.mysql.com/doc/
```

Reglas de calidad:

- usar búsqueda web si está disponible cuando la respuesta pueda estar
  desactualizada (versiones, precios, estado de herramientas) o cuando
  no haya certeza;
- no inventar: si no se conoce la respuesta con seguridad, escribir
  `→ Respuesta: sin información confiable` en lugar de adivinar;
- no responder con opinión personal ni elegir por el usuario;
- no modificar la pregunta ni mezclar la respuesta con el texto del
  usuario;
- responder en el idioma y el registro de la nota.
