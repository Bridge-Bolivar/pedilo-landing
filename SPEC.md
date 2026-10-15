# Landing global de Pedilo · `pedilo.net`

Estado: **approved** (Manuel, 2026-10-15). Carril: integrations.

## Problema / por qué

`pedilo.net` es el dominio de la marca y hoy muestra "Account Suspended" (hosting compartido
caído). Pedilo tiene dos productos, Delivery y Market, cada uno con su subdominio. Hace falta
una puerta de entrada única que presente la marca y lleve a cada app.

## Objetivo

Una sola pantalla, estática, rápida y prolija, que:

1. Presente qué es Pedilo en una frase.
2. Muestre las dos apps como dos tarjetas iguales en jerarquía, con qué hace cada una, para
   quién es, y un botón que lleva a su subdominio.
3. Cierre con contacto y links legales.

Sin login, sin formularios, sin JavaScript obligatorio, sin dependencias de build. Un archivo
`index.html` con CSS embebido y los assets al lado.

## Historias

- Como vecino de Bolívar que escuchó "Pedilo", entro a `pedilo.net` y en cinco segundos entiendo
  qué es y a cuál de las dos apps ir.
- Como comercio, veo que Pedilo es una marca con dos servicios y elijo el que me sirve.
- Como integrante del equipo, tengo un lugar que representa la marca entera para mandar por
  WhatsApp o poner en un QR.

## Criterios de aceptación

- Carga en menos de 1 s en un celular con 3G: HTML menor a 30 KB sin contar imágenes, una sola
  imagen grande (el logo), fuentes del sistema o una sola familia web.
- Se ve bien de 320 px a 1440 px, sin scroll horizontal.
- Los dos botones apuntan a `https://delivery.pedilo.net` y `https://market.pedilo.net`.
- Título, descripción y OG image para que el link se vea bien en WhatsApp.
- Contraste AA en todos los textos. Accesible por teclado.
- El pie tiene contacto (WhatsApp y mail) y links a términos y privacidad.

## Identidad

- Logo: la burbuja con la P en ámbar (`assets/logo.png`), el mismo de la app de Delivery.
- Fondo crema `#faf6f1` y tinta `#1c1917`, los tokens de la app.
- Acento de cada tarjeta: Delivery bordó `#9a0002` (el `--brand-primary` de la app); Market
  verde `#013e37` (la paleta de su presentación). Así cada app conserva su color sin que la
  landing sea de ninguna de las dos.
- Tipografía: Inter, la misma de la app.
- Español rioplatense, voseo, frases cortas.

## Fuera de alcance

- Blog, noticias, formularios de contacto, analítica.
- Páginas legales propias: por ahora linkean a las de Delivery.
- Diseño de la landing de Market: cuando Market se despliegue en `market.pedilo.net`, el botón
  ya apunta ahí.

## Preguntas abiertas

- WhatsApp y mail de contacto definitivos (hoy hay placeholders marcados con `TODO`).
- Si `www.pedilo.net` redirige a `pedilo.net` (propuesto: sí).
