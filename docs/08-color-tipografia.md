# Color y tipografía — Construcciones Maibru SpA

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

| Rol | Color | HEX | Uso |
|---|---|---|---|
| Principal | Azul cielo | `#00BFFF` | Franjas de tarjetas, líneas de acento y detalles de marca. Siempre con texto oscuro si lleva texto encima. |
| Secundario | Verde claro | `#8FCB5E` | Franjas de tarjetas y detalles. Siempre con texto oscuro si lleva texto encima. |
| Acento | Verde vivo | `#66C21A` | Botón de WhatsApp y de contacto, y llamados a la acción. Texto oscuro encima. |
| Principal oscuro | Azul profundo | `#00719C` | Títulos destacados, enlaces, bordes de botones secundarios y botones con texto blanco. |
| Acento oscuro | Verde profundo | `#3F7D0B` | Textos de apoyo y detalles sobre fondo claro. |
| Neutro | Fondo | `#FFFFFF` | Fondo general del sitio. |
| Neutro | Gris claro | `#D9DEDE` | Secciones alternadas y bordes. |
| Neutro | Texto principal | `#1F2933` | Títulos y párrafos. |
| Neutro | Texto secundario | `#52606D` | Descripciones y textos de apoyo. |
| Estado | Éxito | `#1B7F3B` | Confirmaciones. |
| Estado | Error | `#B3261E` | Mensajes de error. |

## Contraste

| Combinación | Ratio | Resultado |
|---|---|---|
| Texto principal sobre blanco | 14.7:1 | Sí |
| Texto principal sobre azul cielo | 7.0:1 | Sí |
| Texto principal sobre verde vivo | 6.5:1 | Sí |
| Texto principal sobre verde claro | 7.7:1 | Sí |
| Texto principal sobre gris claro | 10.9:1 | Sí |
| Texto secundario sobre blanco | 6.5:1 | Sí |
| Azul profundo sobre blanco | 5.5:1 | Sí |
| Texto blanco sobre azul profundo | 5.5:1 | Sí |
| Texto blanco sobre error | 6.5:1 | Sí |
| Texto blanco sobre azul cielo o verde vivo (evitar) | 2.1:1 a 2.3:1 | No |

### Reglas de uso

- Los fondos grandes del sitio son blancos o gris claro, y los colores de la paleta se usan como detalles (botones, franjas, líneas de acento y títulos) para mantener un aspecto luminoso.
- Sobre los colores vivos siempre va texto oscuro. El texto blanco solo se usa sobre los tonos profundos.
- El logo de la empresa va a la izquierda del menú superior, y de él salen el azul y el verde de la paleta.
- Las tarjetas de servicios alternan sus franjas de color: verde claro, azul cielo y verde vivo.
- La portada (hero) lleva de fondo una fotografía real de un trabajo de la empresa, con una capa oscura semitransparente (`#1F2933` al 55 %) encima para que el texto blanco se lea bien. Es la única sección con foto de fondo; el resto del sitio mantiene fondos blancos o gris claro.

## Tipografía

| Uso | Fuente | Peso |
|---|---|---|
| Títulos | Montserrat | Bold (700) |
| Texto y botones | Open Sans | Regular (400) y SemiBold (600) |


| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| h1 | 40 px | 32 px | Bold |
| h2 | 32 px | 28 px | Bold |
| h3 | 24 px | 20 px | Bold |
| Párrafo | 16 px | 16 px | Regular |
| Botón | 16 px | 16 px | SemiBold |

## Justificación

Montserrat es ancha, gruesa y sin adornos, similar a la letra del logo, y transmite solidez y profesionalismo. Open Sans es sencilla y muy legible, pensada para que Camila lea con comodidad desde el celular. El texto no baja de 16 px para evitar tener que hacer zoom.