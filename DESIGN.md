---
name: Pedilo
description: La puerta de San Carlos de Bolívar. El hub no tiene color propio.
colors:
  dot: "#df5550"
  ash: "#2c2a28"
  ink: "#1c1917"
  muted: "#6e665e"
  bone: "#f3f0eb"
  paper: "#f6f3ee"
  field: "#e6e1d8"
  well: "#d9d3cb"
typography:
  display:
    fontFamily: "system-ui, \"Segoe UI\", Roboto, sans-serif"
    fontSize: "clamp(36px, 5vw, 44px)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.05em"
  headline:
    fontFamily: "system-ui, \"Segoe UI\", Roboto, sans-serif"
    fontSize: "clamp(26px, 4vw, 40px)"
    fontWeight: 500
    lineHeight: 1.35
    letterSpacing: "-0.03em"
  title:
    fontFamily: "system-ui, \"Segoe UI\", Roboto, sans-serif"
    fontSize: "18px"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.03em"
  body:
    fontFamily: "system-ui, \"Segoe UI\", Roboto, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "normal"
  label:
    fontFamily: "system-ui, \"Segoe UI\", Roboto, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.12em"
rounded:
  card: "22px"
  card-phone: "18px"
  photo: "16px"
  photo-phone: "13px"
  sheet: "28px"
  focus: "8px"
  control: "999px"
spacing:
  card-pad: "8px"
  cluster: "32px"
  frame: "22px 16px"
components:
  brand:
    textColor: "{colors.bone}"
    typography: "{typography.display}"
    padding: "0"
  brand-focus:
    textColor: "{colors.bone}"
    rounded: "8px"
    padding: "0"
  product-card:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "{spacing.card-pad}"
  icon-chip:
    backgroundColor: "{colors.ash}"
    textColor: "{colors.bone}"
    rounded: "{rounded.control}"
    size: "32px"
  sheet:
    backgroundColor: "{colors.bone}"
    textColor: "{colors.ink}"
    rounded: "28px"
    padding: "72px 7vw 28px"
---

# Design System: Pedilo

## Overview

**Creative North Star: "La puerta de la ciudad"**

Pedilo en este sitio es una puerta, no una explicación. Alguien llega y elige. El fondo es una foto real del puente colgante de San Carlos de Bolívar, en blanco y negro y oscurecida. El lockup y las dos tarjetas viven juntos en el centro, en hueso, para que la ciudad se lea detrás.

El hub no toma el bordó de Delivery ni el verde de Market. Esos colores pertenecen a cada producto. Acá la página es ceniza, hueso y un solo acento: el punto de `pedilo.`

**Key Characteristics:**

- Foto real, nunca una escena generada.
- Lockup horizontal: isotipo claro a la izquierda de `pedilo.` y el punto bordó.
- Dos tarjetas, lado a lado también en el celular.
- El centro de la foto va más oscuro que el resto, para que el texto claro se lea.

## Colors

Ceniza, hueso y un punto. Nada más pinta la página.

### Primary

- **Punto bordó** (`{colors.dot}`): solo el punto de `pedilo.` Sobre el cielo oscuro tiene que seguir leyéndose. No se usa como fondo de botón ni como relleno de tarjeta.

### Neutral

- **Ceniza** (`{colors.ash}`): los círculos de ícono sobre la foto, la selección de texto, la barra de scroll.
- **Tinta** (`{colors.ink}`): texto sobre hueso y sobre papel.
- **Apagado** (`{colors.muted}`): la descripción de cada tarjeta, el pie y la línea de «Escribinos».
- **Hueso** (`{colors.bone}`): la palabra del lockup, el lugar, la hoja de abajo y el anillo de foco.
- **Papel** (`{colors.paper}`): el cuerpo de las tarjetas. Un paso más claro que la hoja.
- **Campo** (`{colors.field}`): el fondo de la página cuando la hoja todavía no lo tapa.
- **Pozo** (`{colors.well}`): el vacío de la foto hasta que haya una imagen.

**The Hub Stays Neutral Rule.** Delivery y Market no pintan `pedilo.net`. Su color vive en el subdominio, no en esta pantalla.

**The Readable Sky Rule.** El texto claro se apoya en cielo oscurecido. El lugar va en hueso sólido. El punto bordó necesita un fondo cerca de la ceniza, no un gris medio.

## Typography

**Display Font:** system-ui (con Segoe UI, Roboto, sans-serif)
**Body Font:** la misma pila

**Character:** Una sola sans del sistema. El carácter lo pone el lockup, no una tipografía de exhibición.

### Hierarchy

- **Display** (700, `clamp(36px, 5vw, 44px)`, line-height 1): la palabra `pedilo.`
- **Headline** (500, `clamp(26px, 4vw, 40px)`, line-height 1.35): el párrafo de la hoja.
- **Title** (700, 18px, line-height 1.15): el título de cada tarjeta. En el celular baja a 15px.
- **Body** (400, 18px, line-height 1.4): «Escribinos» y el cuerpo general.
- **Label** (600, 13px, tracking 0.12em, mayúsculas): «San Carlos de Bolívar». En el celular, 11px.
- En el celular el display baja a 34px (30px si la pantalla es corta), el título de tarjeta a 15px, la descripción a 12px y el pie a 14px.

**The One Face Rule.** No se carga una webfont para esta página. Si el lockup pide otra voz, se decide aparte y se autoaloja.

## Layout

La primera pantalla es `100dvh` y sticky. La foto la cubre. El lockup y las tarjetas son una columna centrada en los dos ejes, con 32px entre ellos (20px por debajo de 680px). Las tarjetas miden como máximo 560px y se parten en dos columnas iguales, también en el celular, para que el puente siga viéndose. Al scrollear, una hoja sube y tapa la foto.

## Elevation & Depth

La profundidad es poca y siempre hacia abajo: la tarjeta flota sobre la foto y la hoja flota sobre la pantalla. No hay halo de color.

### Shadow Vocabulary

- **Tarjeta** (`box-shadow: 0 14px 36px rgb(12 16 14 / 0.28)`): la pareja de tarjetas sobre el puente.
- **Hoja** (`box-shadow: 0 -28px 70px rgb(20 18 16 / 0.28)`): el borde superior de la hoja al subir.

**The Downward Shadow Rule.** La sombra cae. No se usa un bloque duro sin blur ni un resplandor de color.

## Shapes

Las tarjetas cierran a 22px (18px en el celular). La foto de adentro cierra a 16px (13px en el celular) y no llega al borde de la tarjeta: el papel se ve en la curva, y por eso el redondeo no se ve rasposo. Los íconos sobre la foto son círculos. El foco del logo cierra a 8px. La hoja redondea solo arriba, a 28px.

## Components

### Navigation

El lockup es el único elemento de marca. Isotipo claro (`assets/mark.png`) a la izquierda de la palabra, punto bordó a la derecha. Debajo, el lugar con el pin de Phosphor en duotono. El foco del logo es un anillo de hueso de 3px.

### Cards / Containers

- **Corner Style:** 22px la tarjeta, 16px la foto.
- **Background:** papel. La foto es el contenido, con un pozo `#d9d3cb` mientras no hay imagen.
- **Shadow Strategy:** la sombra de tarjeta.
- **Border:** ninguno.
- **Internal Padding:** 8px alrededor de la foto, 14px abajo.
- Arriba a la izquierda de la foto, un círculo ceniza con un ícono Phosphor lleno (cubiertos o vidriera). Arriba a la derecha, el mismo círculo con la flecha para entrar. El nombre de la puerta va debajo de la foto, a la izquierda, y después el título y una línea.

### [La hoja]

Sube al scrollear. Fondo hueso, texto tinta, una sola medida corta. El pie lleva el mail y los legales, con área de toque de 44px.

## Do's and Don'ts

### Do:

- **Do** usar el isotipo claro sobre el cielo oscuro y el rojo solo sobre cielo claro.
- **Do** dejar el punto bordó como único acento del hub.
- **Do** mantener las dos tarjetas lado a lado en el celular.
- **Do** hornear el blur de la foto. No desenfocar con CSS.

### Don't:

- **Don't** pintar la página con el bordó de Delivery ni el verde de Market.
- **Don't** apilar el isotipo arriba de la palabra.
- **Don't** recortar la foto justo en la esquina de la tarjeta.
- **Don't** bajar la opacidad del lugar para «suavizarlo».
