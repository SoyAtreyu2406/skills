# Ejemplo: nota técnica con comandos, salida, URL y código

## Antes

```text
para ver la ip uso ipconfig. me da Adaptador de LAN inalámbrica Wi-Fi: Dirección IPv4 : 192.168.1.105
despues pruebo desde el celu http://192.168.1.105:4321
el codigo que pruebo es function sumar(a,b){const r=a+b;return r}
```

## Después

```text
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  PRUEBA DE ACCESO DESDE LA RED
◆━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Para ver la IP uso:

  $ ipconfig

Me da:

  > Adaptador de LAN inalámbrica Wi-Fi:
  >    Dirección IPv4 : 192.168.1.105

Después pruebo desde el celular:

  🔗 http://192.168.1.105:4321

El código que pruebo es:

function sumar(a, b) {
  const r = a + b;
  return r;
}
```

Notas: el código va a columna 0 y sin cercas; la URL se conserva
idéntica; el comando lleva `$` y la salida `>`. Al venir en una sola
línea, el código se separa y se indenta por su estructura (único caso
en que se toca su forma interna).
