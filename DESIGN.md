---
version: alpha
name: "[Nombre del emprendimiento]"
description: "[Design system de ... en una línea]"
# Guía: evaluacion/guias/fase-2-specs/06-spec-de-diseno.md
# Reemplaza TODOS los valores de ejemplo por los de tu paleta y tipografía
# (docs/08-color-tipografia.md). Los HEX van siempre entre comillas.
# Valida con: npx @google/design.md lint DESIGN.md
colors:
  primary: "#1F4E79"
  primary-hover: "#183E60"
  on-primary: "#FFFFFF"
  secondary: "#E8EEF4"
  on-secondary: "#1A1A1A"
  tertiary: "#B5462B"
  on-tertiary: "#FFFFFF"
  neutral: "#FAFAFA"
  surface: "#FFFFFF"
  on-surface: "#1A1A1A"
  on-surface-variant: "#5C5C5C"
  disabled: "#D6D6D6"
  on-disabled: "#4A4A4A"
  error: "#B3261E"
typography:
  headline-display:
    fontFamily: "[Fuente de títulos]"
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
  headline-lg:
    fontFamily: "[Fuente de títulos]"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: "[Fuente de títulos]"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  body-md:
    fontFamily: "[Fuente de textos]"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: "[Fuente de textos]"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
rounded:
  md: 8px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  tag-offer:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.full}"
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---
name: Construcciones Maibru
description: Sitio web de Construcciones Maibru SpA, empresa de la región de Valparaíso que instala ventanas (PVC, termopanel, aluminio y vidrio templado) y realiza remodelaciones de viviendas. El contacto es directo por WhatsApp, teléfono o correo.
colors:
  primary: "#00719C"
  on-primary: "#FFFFFF"
  sky: "#00BFFF"
  secondary: "#8FCB5E"
  accent: "#66C21A"
  on-accent: "#1F2933"
  accent-deep: "#3F7D0B"
  on-accent-deep: "#FFFFFF"
  surface: "#FFFFFF"
  surface-alt: "#D9DEDE"
  text: "#1F2933"
  text-muted: "#52606D"
  overlay: "#1F2933"
  on-overlay: "#FFFFFF"
  success: "#1B7F3B"
  error: "#B3261E"
typography:
  h1:
    fontFamily: Montserrat
    fontSize: 40px
    fontWeight: 700
    lineHeight: 1.2
  h1-mobile:
    fontFamily: Montserrat
    fontSize: 32px
    fontWeight: 700
    lineHeight: 1.2
  h2:
    fontFamily: Montserrat
    fontSize: 32px
    fontWeight: 700
    lineHeight: 1.25
  h2-mobile:
    fontFamily: Montserrat
    fontSize: 28px
    fontWeight: 700
    lineHeight: 1.25
  h3:
    fontFamily: Montserrat
    fontSize: 24px
    fontWeight: 700
    lineHeight: 1.3
  h3-mobile:
    fontFamily: Montserrat
    fontSize: 20px
    fontWeight: 700
    lineHeight: 1.3
  body-md:
    fontFamily: Open Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Open Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  button:
    fontFamily: Open Sans
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.2
rounded:
  sm: 4px
  md: 8px
  lg: 12px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 40px
  section: 64px
components:
  navbar:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    height: 72px
    padding: 16px
  navbar-link-active:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.button}"
  hero:
    backgroundColor: "{colors.overlay}"
    textColor: "{colors.on-overlay}"
    typography: "{typography.body-md}"
    padding: 64px
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.on-accent}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
    height: 44px
    padding: 12px
  button-primary-hover:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-accent}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
  button-primary-active:
    backgroundColor: "{colors.accent-deep}"
    textColor: "{colors.on-accent-deep}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
  button-primary-disabled:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.text-muted}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
    height: 44px
    padding: 12px
  button-secondary-hover:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
  whatsapp-flotante:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.on-accent}"
    typography: "{typography.button}"
    rounded: "{rounded.full}"
    height: 56px
    padding: 12px
  tarjeta-servicio:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 24px
  tarjeta-producto:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 16px
  filtro-catalogo:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 16px
  chip:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.text}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 8px
  chip-activo:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 8px
  tarjeta-proyecto:
    backgroundColor: "{colors.overlay}"
    textColor: "{colors.on-overlay}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.md}"
    padding: 16px
  tarjeta-proyecto-ubicacion:
    backgroundColor: "{colors.overlay}"
    textColor: "{colors.accent}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.md}"
  bloque-confianza:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    padding: 40px
  tarjeta-experiencia:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 24px
  tarjeta-articulo:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 16px
  footer:
    backgroundColor: "{colors.surface-alt}"
    textColor: "{colors.text}"
    typography: "{typography.body-sm}"
    padding: 40px
---

# Construcciones Maibru — Design System

## Overview

Construcciones Maibru es una empresa familiar de la región de Valparaíso que instala ventanas (PVC, termopanel, aluminio y vidrio templado) y remodela viviendas. El sitio existe para que una persona conozca los servicios, vea trabajos reales y contacte rápido a la empresa por WhatsApp, teléfono o correo.

La proto-persona es Camila, 38 años, trabajadora independiente y dueña de casa. Busca desde el celular a alguien confiable y quiere información clara. Por eso la personalidad visual es **confiable, sólida, clara, cercana y luminosa**: un estilo limpio, con mucho espacio en blanco y fotografías reales de trabajos, que se ve profesional sin parecer frío.

El sitio no tiene carrito ni cotizador. Toda la conversión ocurre en el contacto directo, así que el botón de WhatsApp es el elemento más importante de cada pantalla.

## Colors

- **Azul profundo (`primary`, #00719C):** títulos destacados, enlaces, bordes de botones secundarios y cualquier elemento con texto blanco encima.
- **Azul cielo (`sky`, #00BFFF):** líneas de acento y franjas de tarjetas. Nunca lleva texto blanco encima.
- **Verde claro (`secondary`, #8FCB5E):** franjas de tarjetas, estado hover del botón principal y detalles.
- **Verde vivo (`accent`, #66C21A):** botón de WhatsApp, llamados a la acción y la ubicación en las tarjetas de proyecto. Siempre con texto oscuro (`on-accent`) cuando es un botón.
- **Verde profundo (`accent-deep`, #3F7D0B):** estado activo (presionado) del botón principal y textos de apoyo sobre fondo claro.
- **Neutros:** fondo blanco (`surface`), gris claro (`surface-alt`) para secciones alternadas, texto principal (`text`) y texto secundario (`text-muted`).
- **Estados:** éxito (`success`) y error (`error`) para mensajes.

Reglas de contraste: sobre los colores vivos (azul cielo, verde vivo, verde claro) va siempre texto oscuro. El texto blanco solo se usa sobre azul profundo, verde profundo, error y la capa oscura del hero y de las tarjetas de proyecto. Todas las combinaciones cumplen contraste mínimo AA (4.5:1).

Los fondos grandes son blancos o gris claro. Las únicas excepciones son el **Hero** y las **Tarjetas de proyecto**, que llevan una fotografía real de un trabajo de la empresa con una capa oscura (`overlay`) para que el texto se lea bien.

## Typography

- **Títulos:** Montserrat Bold (700). Es ancha, sólida y sin adornos, parecida a la letra del logo.
- **Texto y botones:** Open Sans Regular (400) y SemiBold (600). Es sencilla y muy legible en el celular.
- Ambas fuentes son de Google Fonts.

| Elemento | Escritorio | Celular |
|---|---|---|
| h1 | 40 px | 32 px |
| h2 | 32 px | 28 px |
| h3 | 24 px | 20 px |
| Párrafo | 16 px | 16 px |
| Botón | 16 px SemiBold | 16 px SemiBold |

El texto de lectura no baja de 16 px, para que Camila no tenga que hacer zoom. Los párrafos largos (artículos del blog) no superan unos 70 caracteres por línea.

## Layout

- **Escritorio (1200 px o más):** contenido centrado con ancho máximo de 1200 px y cuadrícula de 12 columnas. Las tarjetas se muestran de 3 en 3.
- **Tablet (768 a 1199 px):** cuadrícula de 8 columnas. Las tarjetas se muestran de 2 en 2.
- **Mobile (375 px de referencia):** una sola columna con márgenes laterales de 16 px. El menú del navbar se convierte en un botón de menú (hamburguesa), las tarjetas pasan a una columna y los botones ocupan el ancho completo.
- **Espaciado:** escala de 4, 8, 16, 24 y 40 px entre elementos, y 64 px entre secciones.
- **Orden:** cada pantalla repite la misma estructura: Navbar arriba, contenido en bloques separados por espacio generoso, Footer al final y el Botón flotante de WhatsApp fijo en la esquina inferior derecha.
- **Mobile-first:** la prioridad es el celular, así que los botones tienen un alto mínimo de 44 px para tocarse con facilidad.

## Elevation & Depth

El estilo es plano y limpio. La profundidad se logra con bordes finos y sombras muy suaves, nunca con sombras marcadas.

- **Tarjetas:** borde de 1 px gris claro y, al pasar el mouse, sombra suave (0 2px 8px con el color de texto al 8 % de opacidad).
- **Navbar:** queda fijo arriba al hacer scroll, con una línea inferior gris claro.
- **Botón flotante de WhatsApp:** lleva una sombra un poco más marcada para destacar sobre el contenido.
- **Hero:** la capa oscura sobre la foto da contraste al texto.
- **Tarjetas de proyecto:** la foto lleva un degradado oscuro en la parte inferior (del color `overlay`, transparente arriba y opaco abajo) para que el nombre y la ubicación se lean bien.

## Shapes

- **Botones y tarjetas:** esquinas redondeadas medias (8 px).
- **Chips y filtros:** esquinas redondeadas completas (forma de píldora).
- **Botón flotante de WhatsApp:** circular o de píldora.
- **Fotos:** esquinas de 8 px, sin marcos ni bordes gruesos.
- **Franjas de color:** de 5 px de alto en la parte superior de las tarjetas de servicio, en azul cielo, verde claro y verde vivo.

## Components

### Navbar
Logo de Construcciones Maibru a la izquierda, menú (Inicio, Servicios, Catálogo, Proyectos, Blog, Contacto) y un botón principal "Contáctanos". La página activa se marca con color azul profundo. Queda fijo arriba. En mobile se reemplaza el menú por un botón de menú.

### Hero
Foto de fondo de un trabajo real con capa oscura, título en blanco, texto breve y dos botones: el principal de WhatsApp ("Pedir presupuesto por WhatsApp") y el secundario ("Ver trabajos"). Es uno de los dos componentes con foto de fondo.

### Botón principal (WhatsApp)
Fondo verde vivo, texto oscuro, 44 px de alto y esquinas de 8 px.
- **Normal:** verde vivo.
- **Hover:** verde claro.
- **Activo (presionado):** verde profundo con texto blanco.
- **Deshabilitado:** gris claro con texto gris.
El mensaje de WhatsApp siempre sale predefinido, y en las fichas de producto menciona el producto consultado.

### Botón secundario
Fondo blanco, borde y texto azul profundo. En hover se invierte (fondo azul profundo y texto blanco).

### Tarjeta de servicio
Franja de color arriba, nombre en Montserrat, texto breve de una o dos líneas y, si corresponde, un enlace "Ver más". Se muestran tres: Ventanas, Vidrio templado y Remodelaciones.

### Tarjeta de producto
Foto, nombre del producto (máximo 2 líneas), etiqueta de material y dos botones: "Ver detalle" y "Consultar por WhatsApp". No se muestran precios en ninguna parte: el precio se consulta por contacto directo.

### Filtro de catálogo
Barra de búsqueda por nombre y filtros por material (PVC, termopanel, aluminio, vidrio templado) y tipo de apertura (corredera, abatible, proyectante, fija). Los filtros activos se muestran como chips con fondo azul profundo.

### Galería de proyectos
Sección "Portafolio de proyectos" sobre fondo blanco, con una cuadrícula de 6 tarjetas (3x2 en escritorio, 2 en tablet y 1 en mobile). Cada Tarjeta de proyecto tiene esquinas de 8 px, una fotografía real del trabajo y un degradado oscuro en la parte inferior con dos líneas de texto: el nombre del proyecto en blanco y negrita, y la ubicación en verde vivo. Todas las fotos llevan texto alternativo.

### Bloque de confianza
Tres mensajes breves sobre fondo gris claro: producto e instalación, atención directa y presupuesto a medida.

### Tarjeta de experiencia
Nombre del cliente, tipo de trabajo y opinión breve. Solo se publican experiencias reales y autorizadas por el cliente.

### Tarjeta de artículo
Imagen, etiqueta de categoría, título (máximo 3 líneas) y enlace "Leer más". Se usa en la landing, el blog y los artículos relacionados.

### Footer
Logo, teléfono, WhatsApp, correo, comunas de cobertura de la región de Valparaíso y enlaces a Instagram y Facebook.

### Botón flotante de WhatsApp
Fijo en la esquina inferior derecha, visible en todas las páginas y con el mensaje predefinido. En mobile no tapa el contenido importante.

## Do's and Don'ts

**Do**
- Usa el botón de WhatsApp como llamado a la acción principal en cada pantalla.
- Usa fotos reales de trabajos de la empresa.
- Mantén fondos blancos o gris claro y usa los colores vivos como detalles.
- Usa texto oscuro sobre azul cielo, verde vivo y verde claro.
- Mantén todo el texto de lectura en 16 px o más.
- Agrega texto alternativo (`alt`) a todas las imágenes.
- Usa los mismos nombres de componentes en todas las pantallas.

**Don't**
- No uses texto blanco sobre azul cielo, verde vivo ni verde claro.
- No muestres precios, carrito ni formularios de cotización.
- No uses más de dos tipografías.
- No uses fondos de color grandes, salvo la foto con capa oscura del Hero y los degradados oscuros sobre las fotos de las tarjetas de proyecto.
- No uses sombras fuertes ni bordes gruesos.
- No publiques testimonios inventados ni fotos que no sean de la empresa.