# Spec de desarrollo — Construcciones Maibru SpA

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Eres un desarrollador front-end. Vas a construir el sitio web estático de Construcciones Maibru SpA, una empresa de la región de Valparaíso que instala ventanas (PVC, termopanel, aluminio y vidrio templado) y hace remodelaciones de viviendas. El contacto es directo por WhatsApp, teléfono o correo. La persona que usará el sitio es Camila, 38 años, trabajadora independiente y dueña de casa, que busca desde el celular a alguien confiable y quiere información clara.

ARCHIVOS QUE DEBES LEER ANTES DE ESCRIBIR CÓDIGO
1. DESIGN.md (raíz): design system con colores, tipografía, espaciado, formas, componentes y reglas Do's and Don'ts. Es la única fuente de valores visuales.
2. docs/01-brief.md, docs/02-proto-personas.md y docs/03-funcionalidades.md: quién es el cliente y qué debe poder hacer en el sitio.
3. docs/04-tecnologias.md: stack, qué es funcional y qué es prototipo, e integraciones futuras.
4. docs/05-arquitectura.md: mapa del sitio, user flows y categorías de productos y de blog.
5. docs/07-componentes.md, docs/08-color-tipografia.md y docs/09-spec-diseno.md: componentes calcados, paleta y prompts de cada pantalla.
6. La carpeta stitch/: código HTML exportado de los prototipos de Stitch. Úsalo como referencia visual de cada pantalla, no como código final.

REGLAS TÉCNICAS
- Solo HTML5, CSS3 y JavaScript básico. Sin frameworks, sin librerías, sin CMS ni base de datos. Debe funcionar en GitHub Pages.
- Sigue exactamente la estructura de archivos y carpetas de la sección 2 de este documento.
- Usa HTML semántico (header, nav, main, section, article, aside, footer) y un solo h1 por página.
- Todos los colores, fuentes, tamaños, espaciados y radios salen de variables CSS en :root, copiadas de los tokens de DESIGN.md. No escribas valores sueltos en las reglas.
- Diseño mobile-first, con min-width y los breakpoints de la sección 5.
- Usa los mismos nombres de componentes que DESIGN.md y las clases de la sección 5.
- Todos los enlaces y recursos usan rutas relativas.
- Las fuentes (Montserrat 700 y Open Sans 400 y 600) se cargan desde Google Fonts con font-display: swap.

REGLAS DE CONTENIDO
- No hay carrito, precios ni formularios de cotización. Toda consulta termina en un enlace de WhatsApp (wa.me) con mensaje predefinido, un enlace tel: o un enlace mailto:.
- No inventes datos. Donde falte un dato real (teléfono, correo, comunas, opiniones de clientes, nombres de proyectos), deja un marcador visible entre corchetes, como [TELÉFONO], y avísame al terminar la página.
- Las opiniones de clientes y los comentarios de ejemplo se marcan con la etiqueta "Ejemplo".
- Todas las imágenes llevan atributo alt descriptivo, width y height, y loading="lazy" (salvo la imagen del hero).
- Lo que es prototipo visual (filtros, búsqueda, comentarios y navegación por categorías del blog) se maqueta sin lógica de servidor, como indica docs/04-tecnologias.md.

CÓMO TRABAJAR
1. Crea primero la estructura de carpetas, css/styles.css (variables, reset, base y componentes compartidos) y js/main.js.
2. Construye una página por vez, en este orden: index.html, catalogo.html, producto.html, contacto.html, blog.html, articulo.html, y después las páginas secundarias.
3. Al terminar cada página, revisa los criterios de aceptación (sección 7) y dime cuáles cumple y cuáles no.
4. Si algo no está definido en los documentos, pregúntame antes de decidir.
5. No agregues funcionalidades, secciones ni dependencias que no estén en los documentos.
```

## 1. Estructura de archivos

```text
mi-emprendimiento/
├── DESIGN.md                    Design system (formato Stitch)
├── index.html                   Landing
├── catalogo.html                Tienda (catálogo con filtros)
├── producto.html                Ficha de producto
├── contacto.html                Contacto
├── blog.html                    Blog
├── articulo.html                Artículo
├── servicios.html               Servicios (instalación y remodelaciones)
├── proyectos.html               Galería completa de proyectos
├── sobre-nosotros.html          Empresa y cobertura
├── preguntas-frecuentes.html
├── terminos.html                Términos y condiciones
├── privacidad.html              Política de privacidad
├── 404.html
├── css/
│   └── styles.css               Único archivo de estilos
├── js/
│   └── main.js                  Único archivo de JavaScript
├── img/
│   ├── logo.png                 Logo de la empresa
│   ├── hero-trabajo.jpg         Foto de fondo del hero
│   ├── proyectos/               Fotos de trabajos realizados
│   ├── productos/               Fotos de ventanas y vidrios
│   └── blog/                    Imágenes de artículos
├── stitch/                      Código exportado de Stitch (referencia)
├── docs/                        Documentos de las fases 1 y 2
│   └── img/                     Capturas de moodboard y wireframes
└── evaluacion/                  Guías de la evaluación
```

**Convenciones de nombres:** archivos en minúscula, sin tildes ni espacios, separados con guion (`hero-trabajo.jpg`). Las imágenes de productos se nombran por producto (`ventana-pvc-corredera.jpg`).

**Peso y tamaño de imágenes:**

| Imagen | Tamaño | Peso máximo |
|---|---|---|
| Hero | 1600 x 900 px | 300 KB |
| Fotos de proyectos y productos | 800 x 600 px | 120 KB |
| Imágenes de artículos | 1200 x 630 px | 150 KB |
| Logo | 400 px de ancho, fondo transparente | 50 KB |
```

## 2. Páginas y navegación

### Lista de páginas

| Página | Archivo | `<title>` | Se llega desde | Enlaza a |
|---|---|---|---|---|
| Landing | `index.html` | Construcciones Maibru \| Ventanas y remodelaciones en la región de Valparaíso | Logo y "Inicio" de todas las páginas | Servicios, Catálogo, Proyectos, Blog, Contacto, WhatsApp |
| Catálogo | `catalogo.html` | Catálogo de ventanas y vidrios \| Construcciones Maibru | Navbar, tarjetas de servicio, hero | Ficha de producto, WhatsApp |
| Ficha de producto | `producto.html` | Ventana de PVC corredera \| Construcciones Maibru | Tarjetas de producto | Catálogo (migas), WhatsApp, `tel:`, `mailto:` |
| Contacto | `contacto.html` | Contacto \| Construcciones Maibru | Botón "Contáctanos" | WhatsApp, `tel:`, `mailto:`, Instagram, Facebook, Preguntas frecuentes |
| Blog | `blog.html` | Blog \| Construcciones Maibru | Navbar, landing | Artículo |
| Artículo | `articulo.html` | PVC, aluminio o termopanel: cuál conviene \| Construcciones Maibru | Tarjetas de artículo | Catálogo, Blog (migas), WhatsApp |
| Servicios | `servicios.html` | Servicios \| Construcciones Maibru | Navbar, landing | Catálogo, WhatsApp |
| Proyectos | `proyectos.html` | Proyectos realizados \| Construcciones Maibru | Navbar, "Ver trabajos" | Contacto |
| Sobre nosotros | `sobre-nosotros.html` | Sobre nosotros \| Construcciones Maibru | Footer | Contacto |
| Preguntas frecuentes | `preguntas-frecuentes.html` | Preguntas frecuentes \| Construcciones Maibru | Footer, contacto | Contacto |
| Términos y condiciones | `terminos.html` | Términos y condiciones \| Construcciones Maibru | Footer | Inicio |
| Política de privacidad | `privacidad.html` | Política de privacidad \| Construcciones Maibru | Footer | Inicio |
| 404 | `404.html` | Página no encontrada \| Construcciones Maibru | Enlaces rotos | Inicio, Catálogo |

### Elementos compartidos en todas las páginas

- **Navbar:** logo a la izquierda, menú (Inicio, Servicios, Catálogo, Proyectos, Blog, Contacto) y botón principal "Contáctanos" que lleva a `contacto.html`. La página activa lleva la clase `navbar__link--activo` y `aria-current="page"`. Queda fijo arriba (`position: sticky`).
- **Footer:** logo, descripción de una línea, teléfono, WhatsApp, correo, comunas de cobertura, enlaces a Instagram y Facebook, y enlaces a Sobre nosotros, Preguntas frecuentes, Términos y Privacidad.
- **Botón flotante de WhatsApp:** fijo en la esquina inferior derecha.
- **Salto al contenido:** enlace oculto al inicio que lleva a `#contenido`.

### Enlaces de contacto

| Acción | Formato del enlace |
|---|---|
| WhatsApp general | `https://wa.me/[WHATSAPP]?text=Hola%2C%20quisiera%20consultar%20por%20sus%20servicios` |
| WhatsApp desde la ficha | `https://wa.me/[WHATSAPP]?text=Hola%2C%20quisiera%20consultar%20por%20la%20Ventana%20de%20PVC%20corredera` |
| WhatsApp desde un artículo | `https://wa.me/[WHATSAPP]?text=Hola%2C%20le%C3%AD%20su%20art%C3%ADculo%20y%20quisiera%20una%20asesor%C3%ADa` |
| Teléfono | `tel:+[TELEFONO]` |
| Correo | `mailto:[CORREO]?subject=Consulta%20desde%20el%20sitio%20web` |
| Instagram y Facebook | Enlaces a los perfiles de la empresa, con `target="_blank"` y `rel="noopener"` |

`[WHATSAPP]` y `[TELEFONO]` van en formato internacional sin espacios (por ejemplo, `569XXXXXXXX`).

### Flujos que deben poder recorrerse

1. **Compra:** Inicio → Catálogo → filtro por material → Ficha de producto → Consultar por WhatsApp.
2. **Contenido:** Blog → Artículo → Ver catálogo → Ficha de producto → Consultar por WhatsApp.
3. **Confianza:** Inicio → Proyectos → Contacto (WhatsApp, teléfono o correo).

## 3. Estructura semántica
### Estructura común

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>…</title>
  <meta name="description" content="…">
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <a class="salto" href="#contenido">Saltar al contenido</a>
  <header class="navbar">
    <a class="navbar__logo" href="index.html"><img src="img/logo.png" alt="Construcciones Maibru"></a>
    <button class="navbar__boton" aria-expanded="false" aria-controls="menu">Menú</button>
    <nav id="menu" class="navbar__menu" aria-label="Principal">…</nav>
  </header>
  <main id="contenido">…</main>
  <footer class="footer">…</footer>
  <a class="whatsapp-flotante" href="…" aria-label="Escribir por WhatsApp">…</a>
  <script src="js/main.js"></script>
</body>
</html>
```

### Contenido de `main` por página

| Página | Estructura dentro de `main` |
|---|---|
| Landing | `section.hero` (h1) · `section` Servicios con 3 `article.tarjeta-servicio` · `section` Cómo trabajamos (`ol` de 4 pasos) · `section.bloque-confianza` con 3 mensajes · `section` Portafolio con 6 `article.tarjeta-proyecto` · `section` Experiencias con 3 `article.tarjeta-experiencia` · `section` Blog con 3 `article.tarjeta-articulo` · `section` Cobertura (`ul` de comunas) · `section` Llamado a la acción final |
| Catálogo | `section` Encabezado (h1) · `form.filtro-catalogo` con `role="search"` · `p` contador de resultados · `section` con 6 `article.tarjeta-producto` · `p` estado sin resultados (oculto) · `section` Llamado a la acción |
| Ficha de producto | `nav` migas de pan · `article` con `figure` (galería) y `div` de información (h1, descripción, `ul` de beneficios, selector de variante, botones) · `section` Qué incluye · `section` Acordeón con `details` · `section` Productos relacionados |
| Contacto | `section` Encabezado (h1) · `section` 3 tarjetas de contacto · `section` Horario · `section` Cobertura con mapa · `section` Antes de escribirnos · `section` Redes · `section` Preguntas frecuentes con `details` |
| Blog | `section` Encabezado (h1) · `nav` chips de categoría · `article` Destacado · `section` 6 `article.tarjeta-articulo` · `p` estado sin resultados (oculto) · `section` Llamado a la acción |
| Artículo | `nav` migas de pan · `article` (`header` con h1 y datos, `figure` imagen, cuerpo con h2 y tabla comparativa) · `aside` Compartir · `section` Llamado a la acción · `section` Comentarios · `section` Artículos relacionados |
| Servicios | `section` Encabezado (h1) · 4 `article` por servicio (Ventanas, Vidrio templado, Remodelaciones, Instalación y reemplazo) · `section` Llamado a la acción |
| Proyectos | `section` Encabezado (h1) · galería con 6 o más `article.tarjeta-proyecto` · `section` Llamado a la acción |
| Sobre nosotros | `section` Encabezado (h1) · `section` Quiénes somos · `section.bloque-confianza` · `section` Cobertura |
| Preguntas frecuentes | `section` Encabezado (h1) · lista de `details` · `section` Llamado a la acción |
| Términos y Privacidad | `article` con h1 y secciones h2 |
| 404 | `section` con h1 "Esta página no existe", texto breve y dos botones: "Volver al inicio" y "Ver catálogo" |

### Reglas de semántica

- Un solo `h1` por página. Los títulos siguen el orden h1 → h2 → h3 sin saltos.
- Los botones que abren WhatsApp, llaman o envían correo son `<a>`, no `<button>`.
- Las listas (comunas, beneficios, pasos) usan `<ul>` u `<ol>`.
- Los acordeones usan `<details>` y `<summary>`.
- Cada `section` tiene un título (h2) o un `aria-label`.
- Los íconos decorativos llevan `aria-hidden="true"`.

## 4. Organización del CSS

```css
Un solo archivo, `css/styles.css`, en este orden:

1. Variables (`:root`)
2. Reset y estilos base
3. Tipografía
4. Layout (contenedor, cuadrículas, secciones)
5. Componentes
6. Estilos de páginas específicas
7. Utilidades
8. Media queries

### Variables en `:root` (tokens del `DESIGN.md`)

```css
:root {
  /* Colores */
  --color-primary: #00719C;
  --color-on-primary: #FFFFFF;
  --color-sky: #00BFFF;
  --color-secondary: #8FCB5E;
  --color-accent: #66C21A;
  --color-on-accent: #1F2933;
  --color-accent-deep: #3F7D0B;
  --color-on-accent-deep: #FFFFFF;
  --color-surface: #FFFFFF;
  --color-surface-alt: #D9DEDE;
  --color-text: #1F2933;
  --color-text-muted: #52606D;
  --color-overlay: #1F2933;
  --color-on-overlay: #FFFFFF;
  --color-success: #1B7F3B;
  --color-error: #B3261E;

  /* Tipografía */
  --font-heading: "Montserrat", sans-serif;
  --font-body: "Open Sans", sans-serif;
  --fs-h1: 32px;   /* 40px en escritorio */
  --fs-h2: 28px;   /* 32px en escritorio */
  --fs-h3: 20px;   /* 24px en escritorio */
  --fs-body: 16px;
  --fs-small: 14px;
  --lh-heading: 1.2;
  --lh-body: 1.6;

  /* Formas */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;

  /* Espaciado */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 40px;
  --space-section: 64px;

  /* Otros */
  --shadow-card: 0 2px 8px rgba(31, 41, 51, 0.08);
  --shadow-flotante: 0 4px 12px rgba(31, 41, 51, 0.25);
  --container: 1200px;
  --altura-boton: 44px;
  --altura-navbar: 72px;
}
```

### Convención de nombres

**BEM simplificado**: `bloque`, `bloque__elemento` y `bloque--variante`. Todo en minúscula y en español, con guiones.

### Clases por componente

| Componente (`DESIGN.md`) | Clases |
|---|---|
| Navbar | `.navbar`, `.navbar__logo`, `.navbar__boton`, `.navbar__menu`, `.navbar__link`, `.navbar__link--activo` |
| Hero | `.hero`, `.hero__contenido`, `.hero__titulo`, `.hero__texto`, `.hero__acciones`, `.hero__datos` |
| Botón principal (WhatsApp) | `.btn`, `.btn--principal` |
| Botón secundario | `.btn`, `.btn--secundario` |
| Botón flotante de WhatsApp | `.whatsapp-flotante` |
| Tarjeta de servicio | `.tarjeta-servicio`, `.tarjeta-servicio__franja`, `.tarjeta-servicio__titulo` |
| Tarjeta de producto | `.tarjeta-producto`, `.tarjeta-producto__imagen`, `.tarjeta-producto__etiqueta`, `.tarjeta-producto__acciones` |
| Filtro de catálogo | `.filtro-catalogo`, `.filtro-catalogo__campo`, `.chip`, `.chip--activo` |
| Galería de proyectos | `.galeria`, `.tarjeta-proyecto`, `.tarjeta-proyecto__texto`, `.tarjeta-proyecto__ubicacion` |
| Bloque de confianza | `.bloque-confianza`, `.bloque-confianza__item` |
| Tarjeta de experiencia | `.tarjeta-experiencia`, `.tarjeta-experiencia__cliente` |
| Tarjeta de artículo | `.tarjeta-articulo`, `.tarjeta-articulo__imagen`, `.tarjeta-articulo__categoria` |
| Footer | `.footer`, `.footer__columna` |
| Utilidades | `.contenedor`, `.seccion`, `.seccion--alterna`, `.solo-lectores`, `.oculto`, `.ejemplo` |

### Estados de los botones (según `DESIGN.md`)

| Estado | `.btn--principal` | `.btn--secundario` |
|---|---|---|
| Normal | Fondo verde vivo, texto oscuro | Fondo blanco, borde y texto azul profundo |
| Hover | Fondo verde claro | Fondo azul profundo, texto blanco |
| Activo | Fondo verde profundo, texto blanco | Fondo azul profundo, texto blanco |
| Deshabilitado | Fondo gris claro, texto gris | Fondo gris claro, texto gris |
| Foco (teclado) | Contorno visible de 3 px en azul profundo | Contorno visible de 3 px en azul profundo |

### Breakpoints (mobile-first, con `min-width`)

| Nombre | Ancho | Cambios |
|---|---|---|
| Mobile | Base (375 px de referencia) | Una columna, menú hamburguesa, botones a ancho completo, márgenes de 16 px |
| Tablet | `@media (min-width: 768px)` | Menú horizontal visible, tarjetas de 2 en 2, cuadrícula de 8 columnas |
| Desktop | `@media (min-width: 1200px)` | Contenedor de 1200 px, tarjetas de 3 en 3, títulos a tamaño de escritorio (40, 32 y 24 px) |
```

## 5. Criterios de aceptación

Un solo archivo, `js/main.js`, sin librerías. Cada función se ejecuta solo si el elemento existe en la página.

| Función | Qué hace | Estado |
|---|---|---|
| Menú móvil | Abre y cierra el menú con el botón `.navbar__boton` y actualiza `aria-expanded` | Funcional |
| Año del footer | Escribe el año actual en el texto de copyright | Funcional |
| Copiar enlace | Copia la URL del artículo al portapapeles y muestra "Enlace copiado" | Funcional |
| Filtro y búsqueda del catálogo | Muestra u oculta tarjetas según material y apertura, actualiza el contador "Mostrando X productos" y muestra el estado sin resultados | Prototipo visual |
| Filtro de categorías del blog | Muestra u oculta tarjetas de artículo según el chip activo | Prototipo visual |
| Comentarios del artículo | Agrega el comentario escrito a la lista en pantalla, sin guardarlo | Prototipo visual |
| Mensaje de WhatsApp por producto | Arma el enlace `wa.me` con el nombre del producto leído desde un atributo `data-producto` | Funcional |

**Reglas:** sin `alert()`; mensajes en pantalla; todo debe seguir usable con el teclado.

## 7. Criterios de aceptación

El sitio se considera terminado solo si **todo** lo siguiente se cumple. Se marca cada punto al terminar cada página.

### Contenido y alcance
1. Existen las 13 páginas de la sección 3 y todas se abren sin error.
2. Ninguna página muestra precios, carrito ni formularios de cotización.
3. El catálogo muestra 6 productos y la galería de la landing muestra 6 proyectos, cada uno con foto y título.
4. Cada dato real que falta (teléfono, correo, comunas, opiniones) aparece como marcador entre corchetes, y las opiniones de ejemplo llevan la etiqueta "Ejemplo".

### Navegación
5. Todos los enlaces del Navbar y del Footer llevan a una página que existe.
6. La página activa se marca en el menú con `aria-current="page"`.
7. Los tres flujos de la sección 3 pueden recorrerse de principio a fin sin enlaces rotos.
8. La página 404 permite volver al Inicio y al Catálogo.

### Contacto
9. El botón flotante de WhatsApp aparece en todas las páginas y abre WhatsApp con un mensaje predefinido.
10. En la ficha de producto, el mensaje de WhatsApp menciona el producto consultado.
11. Los enlaces `tel:` y `mailto:` funcionan desde el celular.
12. Los enlaces a Instagram y Facebook abren en una pestaña nueva con `rel="noopener"`.

### Diseño
13. Todos los colores, fuentes, tamaños, espaciados y radios salen de las variables de `:root`; no hay valores sueltos en las reglas.
14. El texto blanco solo aparece sobre azul profundo, verde profundo, error o la capa oscura del hero.
15. El texto sobre azul cielo, verde vivo y verde claro es oscuro.
16. Todo el texto cumple contraste mínimo AA (4.5:1).
17. Solo el hero y las tarjetas de proyecto usan foto con capa o degradado oscuro; el resto tiene fondo blanco o gris claro.
18. Los componentes tienen los estados definidos (normal, hover, activo, deshabilitado y foco).

### Responsivo
19. En 375 px de ancho no hay scroll horizontal.
20. En mobile, el menú se muestra como botón y se puede abrir y cerrar con el mouse y con el teclado.
21. Las cuadrículas de tarjetas pasan a 1 columna en mobile, 2 en tablet y 3 en desktop.
22. El texto de lectura es de 16 px o más y los botones miden al menos 44 px de alto.

### Accesibilidad
23. Todas las imágenes tienen atributo `alt` descriptivo (vacío solo si son decorativas).
24. Todos los elementos interactivos se pueden usar con el teclado y muestran el foco.
25. Existe el enlace "Saltar al contenido" en todas las páginas.

### Calidad del código
26. Cada página tiene un solo `h1` y los títulos siguen el orden h1 → h2 → h3.
27. Cada página tiene `lang="es"`, `<title>` único y `meta description`.
28. El HTML pasa el validador del W3C sin errores.
29. Las imágenes cumplen los pesos máximos de la sección 2.
30. El sitio funciona al publicarse en GitHub Pages, con rutas relativas.
31. No hay frameworks, librerías ni bases de datos: solo HTML, CSS y JavaScript básico.
