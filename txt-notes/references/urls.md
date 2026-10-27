# URLs

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
