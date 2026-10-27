# BLOQUES TÉCNICOS: INDENTACIÓN, CÓDIGO, CONFIGURACIÓN, ÁRBOLES Y TABLAS

## EXCEPCIONES DE INDENTACIÓN

La indentación estructural de la skill organiza la **nota**, pero nunca
debe modificar la indentación interna del contenido técnico original.

La skill debe distinguir entre:

```text
indentación estructural de la nota (2 espacios por nivel jerárquico)
indentación que pertenece al contenido original (se preserva tal cual)
```

### Los bloques técnicos se preservan

Una vez identificado un bloque técnico (código, configuración, estructura
o salida), no agregar, eliminar ni modificar espacios, indentación
interna, saltos de línea, comillas, comillas triples, comentarios,
sintaxis ni ningún otro carácter de su contenido. La indentación
necesaria para representar la jerarquía del documento debe aplicarse al
bloque como unidad, sin alterar su contenido interno.

Esto aplica a:

- código fuente (Python, JS, PHP, etc.);
- scripts y sentencias agrupadas (SQL, shell, procedimientos,
  transacciones);
- archivos de configuración;
- variables de entorno (`.env`);
- JSON;
- YAML;
- XML;
- INI;
- árboles de directorios;
- ejemplos técnicos cuya indentación tenga significado.

En estos bloques **no se modifica absolutamente nada** de su contenido
interno: indentación, espacios, saltos de línea, comillas y la posición
de cada línea respecto de las demás.

### El código es inmutable y no recibe indentación externa

Dentro de esa preservación, el **código** (scripts, sentencias agrupadas,
funciones) tiene un tratamiento especial: además de conservar su
contenido interno intacto, **no se le agrega indentación externa**. El
bloque se entrega tal cual, alineado a columna 0. Las cercas ``` que
delimitan el bloque no forman parte del código.

Esto se debe a que el código puede consumirse o renderizarse con
delimitadores, y los espacios que el formato agregara delante podrían
alterar su significado o su lectura. Los árboles, la configuración y las
salidas sí conservan su indentación externa visual (ver "BLOQUES
INTRODUCIDOS POR DOS PUNTOS"), ya que esa indentación no altera su
estructura.

### Cómo presentar la frase introductoria (código)

La frase que introduce el bloque de código (terminada en `:`) va a columna
0. El bloque se sitúa debajo, también a columna 0 respecto de su
contenido interno, sin que la skill añada indentación externa. La única
separación entre frase y bloque es un renglón vacío.

Ejemplo:

```text
El código que estoy probando es:

function sumar(a, b) {
  const resultado = a + b;
  return resultado;
}

console.log(sumar(10, 20));
```

El contenido técnico se conserva exactamente como en el original, incluso
si alguna de sus líneas está alineada a columna 0. Esto incluye el texto
multilínea dentro de un f-string:

```text
El código es:

def generar_mensaje(nombre):
    """
    Genera un mensaje de bienvenida para el usuario.
    """
    mensaje = f"""
Hola {nombre},
bienvenido al sistema.
Tu cuenta fue creada correctamente.
"""
    return mensaje

print(generar_mensaje("Damian"))
```

Las líneas del texto multilínea quedan menos indentadas que el resto del
código porque así estaban en el original: es preservación fiel, no un
error del formato.

### Código en una sola línea separado en un bloque

Este es el **único caso** en el que el formato modifica la estructura
interna del código.

Cuando el código original aparece en una **sola línea** y conviene
presentarlo como bloque multilínea, no hay indentación original que
preservar: la indentación interna se agrega según la estructura del
código para que se lea bien.

```text
El código que estoy probando es:

function sumar(a, b) {
  const resultado = a + b;
  return resultado;
}

console.log(sumar(10, 20));
```

No se introducen símbolos nuevos ni se cambian valores: solo se separan
las líneas y se indentan los bloques internos del código. El resultado se
entrega también a columna 0.

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

### Excepción: bloques de código

Esta regla de indentación externa NO se aplica a los bloques de código
(scripts, sentencias agrupadas, funciones, código fuente). Esos bloques
se preservan como una unidad inmutable, sin indentación externa, alineados
a columna 0 respecto de su contenido interno (ver "EXCEPCIONES DE
INDENTACIÓN"). El contenido de configuración, JSON, YAML, XML y árboles
conserva su indentación externa visual porque esta no altera su
estructura. La frase que introduce el código queda a columna 0 y el
bloque debajo, separado por un renglón vacío.

```text
El código es:

def generar_mensaje(nombre):
    """
    Genera un mensaje de bienvenida para el usuario.
    """
    mensaje = f"""
Hola {nombre},
bienvenido al sistema.
Tu cuenta fue creada correctamente.
"""
    return mensaje

print(generar_mensaje("Damian"))
```

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

Una vez detectado un bloque de código, no modificar su contenido interno:
indentación, espacios, saltos de línea, comillas y comillas triples se
conservan exactamente como en el original. El bloque es inmutable: no se
le agrega indentación externa y se entrega alineado a columna 0 (ver
"EXCEPCIONES DE INDENTACIÓN").

Los bloques de código se presentan como texto plano, sin cercas ni
símbolos de Markdown: el resultado debe seguir pareciendo una nota
`.txt`, no código renderizado. No usar delimitadores de Markdown (```)
para enmarcar el bloque. La frase que introduce el bloque queda a columna
0 y el código debajo, a columna 0 respecto de su contenido interno,
separado por un renglón vacío.

```text
El código que estoy probando es:

function sumar(a, b) {
  const resultado = a + b;
  return resultado;
}

console.log(sumar(10, 20));
```

El contenido interno del código no recibe indentación externa: esa es la
diferencia con los bloques que sí la reciben (árboles, salidas, comandos
sueltos, URLs). La inmutabilidad prevalece sobre la indentación
estructural de la nota.

Esto también aplica a **scripts y sentencias agrupadas** (SQL, shell,
procedimientos, transacciones, etc.). Un bloque que funciona como una
unidad NO lleva `$` en cada línea: va completo, literal y conserva su
código tal cual (ver "Comandos sueltos vs. bloques de código" en
COMANDOS).

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
