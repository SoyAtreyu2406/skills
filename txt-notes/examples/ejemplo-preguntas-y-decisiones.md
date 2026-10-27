# Ejemplo: preguntas, decisiones y suposiciones

## Antes

```text
reunion con el cliente. decidimos que la web va con astro. creo que el hosting ya lo tiene contratado. que es una landing? el cliente pidio una. no se que es SSR. conviene usar docker? preguntarle a Juan por el logo
```

## Después

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  REUNIÓN CON EL CLIENTE
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

★ La web va a ser con Astro.
~ Creo que el hosting ya lo tiene contratado.

El cliente pidió una landing.

? ¿Qué es una landing?
  → Respuesta: página web de una sola pantalla pensada para que el
    visitante realice una acción concreta (suscribirse, comprar).
  - Ejemplo: página de lanzamiento con un botón "Comprar ahora".

? No sé qué es SSR.
  → Definición: renderizado del lado del servidor; el HTML se genera en
    el servidor en cada pedido, en lugar de en el navegador.

? ¿Conviene usar Docker?
  → Respuesta: depende de cuánto necesites reproducir el entorno.
  - A favor: entorno idéntico en cada máquina, fácil de recrear.
  - En contra: más consumo de recursos y una capa más para depurar.

[ ] Preguntarle a Juan por el logo

Agregué: 1 respuesta, 1 definición, 1 comparación.
```

La última línea queda fuera de la nota.

---

# Contraejemplos (lo que la skill NO debe hacer)

- Inventar secciones como "OBJETIVO" o "PRÓXIMOS PASOS" para esta nota.
- Responder "¿Le pregunto a Juan?" o "¿cuándo es la reunión?": dependen
  del usuario, se dejan como `?` sin respuesta.
- Marcar "podría usar Astro" como `★`: es una posibilidad, no una decisión.
- Endurecer "creo que el hosting ya está contratado" como "el hosting
  está contratado".
- Definir "landing" si el usuario no mostró duda y solo la nombró como
  dato (el cliente pidió una landing).
- Mezclar la respuesta con el texto del usuario o sin `Respuesta:`.
