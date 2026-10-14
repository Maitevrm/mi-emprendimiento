# Spec de diseño — Construcciones Maibru SpA

> Guía: [Spec de diseño](../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)

La spec de diseño tiene dos partes:

1. **[`DESIGN.md`](../DESIGN.md)** (en la raíz): tu design system, en el formato que Stitch importa.
2. **Este documento:** tus pantallas, escritas como prompts listos para pegar en Stitch.

**Wireframes en Whimsical:** https://whimsical.com/duocuc91/wireframes-construcciones-maibru-Go7SXAqxqZpj2xdbJrzTiA

> Guía de wireframes: [Wireframes](../evaluacion/guias/fase-2-specs/04-wireframes.md)

<!-- Captura de los wireframes: ![Wireframes](img/wireframes.png) -->

## Pantallas

<!-- Un prompt por pantalla. Cada uno con: pantalla y dispositivo, objetivo
de tu proto-persona, componentes de arriba hacia abajo (con los nombres de
tu DESIGN.md) y textos y datos reales. -->

### 1. Landing

```text
Pantalla: Landing de Construcciones Maibru, versión desktop. Usa el design system del proyecto.
Objetivo: Camila entiende en pocos segundos qué ofrece la empresa, ve trabajos reales, siente confianza y contacta por WhatsApp. No hay precios, carrito ni formularios de cotización.
Componentes, de arriba hacia abajo:
1. Navbar: logo de Construcciones Maibru a la izquierda, menú (Inicio, Servicios, Catálogo, Proyectos, Blog, Contacto) con "Inicio" marcado como página activa, y botón principal "Contáctanos" a la derecha. Queda fijo arriba al hacer scroll.
2. Hero: foto de fondo de un trabajo real (por ejemplo ventanas de PVC o un cierre de terraza terminado) con capa oscura semitransparente. A la izquierda, sobre la foto: línea pequeña "Región de Valparaíso", título h1 en blanco "Ventanas y remodelaciones en un solo lugar", texto "Producto, instalación y remodelación de viviendas, con atención directa y presupuesto a medida.", botón principal "Pedir presupuesto por WhatsApp" y botón secundario "Ver trabajos". Debajo, una fila de tres datos cortos con ícono de check: "Producto e instalación incluidos", "Atención directa" y "Presupuesto a medida".
3. Servicios: título h2 "Nuestros servicios" y texto "Todo lo que necesitas para renovar tu hogar." Tres Tarjetas de servicio en una fila, cada una con franja de color arriba (azul cielo, verde claro y verde vivo), ícono, nombre, descripción de 2 líneas y enlace "Ver más":
   - "Ventanas": "PVC, termopanel y aluminio con instalación incluida."
   - "Vidrio templado": "Cierres de terraza, shower door y divisiones de ambientes."
   - "Remodelaciones": "Desde una pieza hasta la casa completa, con todas las terminaciones."
4. Cómo trabajamos: título h2 "Así trabajamos" y 4 pasos numerados en una fila: "1. Cuéntanos tu proyecto" (por WhatsApp, teléfono o correo), "2. Coordinamos la visita y las medidas", "3. Fabricamos tu producto a medida" y "4. Instalamos y dejamos todo terminado". Fondo blanco.
5. Bloque de confianza, sobre fondo gris claro: tres mensajes en una fila, cada uno con ícono, título y una frase: "Producto e instalación" (un solo servicio de principio a fin), "Atención directa" (hablas con quien hace el trabajo) y "Presupuesto a medida" (según las necesidades de cada proyecto).
6. Portafolio de proyectos: sección sobre fondo blanco limpio, con título h2 centrado "Portafolio de proyectos" y texto "Algunos de nuestros trabajos realizados." Cuadrícula de 6 tarjetas de proyecto en dos filas de tres (3x2). Cada tarjeta tiene esquinas redondeadas (8 px), una fotografía de alta calidad de un trabajo de construcción o instalación en la parte superior y una superposición de degradado oscuro en la parte inferior que contiene el texto. El texto sigue un formato estricto: en la primera línea el nombre del proyecto en letra blanca y negrita (Montserrat Bold), y en la segunda línea la ubicación en verde vivo (#66C21A). Proyectos de ejemplo: "Ventanas de PVC en vivienda" (Viña del Mar), "Cierre de terraza en vidrio templado" (Concón), "Remodelación completa de casa" (Quilpué), "Ventanales de aluminio" (Valparaíso), "Shower door de vidrio templado" (Villa Alemana) y "Ampliación y terminaciones" (Quilpué). Debajo de la cuadrícula, botón secundario centrado "Ver todos los proyectos".
7. Experiencias de clientes: título h2 "Lo que dicen nuestros clientes" y 3 Tarjetas de experiencia en una fila, cada una con nombre del cliente, tipo de trabajo y opinión de 2 a 3 líneas. Marcarlas como "Ejemplo" hasta tener opiniones reales.
8. Blog: título h2 "Consejos para tu hogar" y 3 Tarjetas de artículo en una fila (imagen, chip de categoría, título y enlace "Leer más"), con los artículos "PVC, aluminio o termopanel: cuál conviene para tu casa", "Claves para planificar la remodelación de tu casa sin sorpresas en el presupuesto" y "Cómo saber cuándo reemplazar tus ventanas y cómo cuidarlas". Debajo, botón secundario "Ver todos los artículos".
9. Zona de cobertura: título h2 "Trabajamos en toda la región de Valparaíso" y chips con las comunas (por ejemplo Valparaíso, Viña del Mar, Concón, Quilpué y Villa Alemana).
10. Llamado a la acción final, sobre fondo gris claro: título h2 "¿Listo para renovar tu hogar?", texto "Escríbenos por WhatsApp y te asesoramos sin compromiso." y botón principal "Pedir presupuesto por WhatsApp", con el teléfono y el correo debajo.
11. Footer: logo, descripción de una línea, teléfono, WhatsApp, correo, comunas de cobertura, enlaces a Instagram y Facebook, y el texto "© Construcciones Maibru SpA".
12. Botón flotante de WhatsApp fijo en la esquina inferior derecha.
```

### 2. Tienda

```text
Pantalla: Catálogo de Construcciones Maibru, versión desktop. Usa el design system del proyecto.
Objetivo: Camila encuentra el tipo de ventana o vidrio que le interesa y lo consulta por WhatsApp, sin precios ni carrito.
Componentes, de arriba hacia abajo:
1. Navbar: igual que en la landing, con "Catálogo" marcado como página activa.
2. Encabezado de página: título "Catálogo de ventanas y vidrios" y texto "Elige el producto que buscas y consúltanos por WhatsApp."
3. Filtro de catálogo, en una barra sobre fondo gris claro con tres controles en una fila:
   - Búsqueda por nombre, con el texto de ayuda "Buscar ventana o vidrio".
   - Material: Todos, PVC, Termopanel, Aluminio, Vidrio templado.
   - Tipo de apertura: Todas, Corredera, Abatible, Proyectante, Fija.
   Debajo, el texto "Mostrando 6 productos" y los filtros activos como chips.
4. Cuadrícula de 6 Tarjetas de producto, en dos filas de tres (3x2). Cada tarjeta tiene foto arriba, nombre (máximo 2 líneas), etiqueta de material, una línea con el tipo de apertura y dos botones: botón secundario "Ver detalle" y botón principal "Consultar por WhatsApp". No muestra precios. Los productos son:
   - "Ventana de PVC corredera", material PVC, apertura corredera.
   - "Ventana de PVC abatible", material PVC, apertura abatible.
   - "Ventana termopanel proyectante", material Termopanel, apertura proyectante.
   - "Ventana de aluminio corredera", material Aluminio, apertura corredera.
   - "Ventanal fijo de aluminio", material Aluminio, apertura fija.
   - "Cierre de terraza en vidrio templado", material Vidrio templado, apertura fija.
5. Estado sin resultados (mostrar como una variante pequeña debajo de la cuadrícula): mensaje "No encontramos productos con esos filtros" y botón secundario "Limpiar filtros".
6. Llamado a la acción: título "¿No encuentras lo que buscas?", texto "Cuéntanos tu proyecto y te asesoramos." y botón principal "Escribir por WhatsApp".
7. Footer: igual que en la landing.
8. Botón flotante de WhatsApp.
```

### 3. Ficha de producto

```text
Pantalla: Ficha de producto de Construcciones Maibru (ejemplo: Ventana de PVC corredera), versión desktop. Usa el design system del proyecto.
Objetivo: Camila conoce el detalle de la ventana, elige las opciones que le interesan y la consulta por WhatsApp con esas opciones ya escritas en el mensaje. No hay precios ni carrito.
Componentes, de arriba hacia abajo:
1. Navbar: igual que en la landing, con "Catálogo" marcado como página activa.
2. Migas de pan: Inicio > Catálogo > Ventana de PVC corredera.
3. Galería del producto (columna izquierda): foto principal grande de la ventana instalada y 4 miniaturas debajo. La miniatura activa lleva un borde azul profundo.
4. Información del producto (columna derecha):
   - Etiqueta de material "PVC".
   - Título h1 "Ventana de PVC corredera".
   - Descripción de 2 a 3 líneas: "Ventana de perfil de PVC con apertura corredera, ideal para dormitorios, living y cocinas. Se fabrica a la medida de tu proyecto e incluye instalación."
   - Lista de 4 beneficios con ícono de check: "Buena aislación térmica y acústica", "Bajo mantenimiento", "Fabricada a medida", "Instalación incluida".
5. Selector de variante, con título "Elige tus opciones":
   - Material: chips "PVC" (seleccionado), "Termopanel", "Aluminio".
   - Tipo de apertura: chips "Corredera" (seleccionado), "Abatible", "Proyectante", "Fija".
   - Tipo de vidrio: chips "Vidrio simple" y "Doble vidrio hermético (termopanel)".
   - Medidas aproximadas: dos campos "Ancho (cm)" y "Alto (cm)".
   - Texto de ayuda debajo: "Las opciones que elijas se incluyen en tu mensaje de WhatsApp."
6. Botones de contacto: botón principal "Consultar por WhatsApp" a ancho completo, con el texto pequeño debajo "Te respondemos a la brevedad", y debajo dos botones secundarios lado a lado: "Llamar" y "Enviar correo".
7. Bloque "¿Qué incluye?": cuatro ítems con ícono: "Producto fabricado a medida", "Retiro de la ventana antigua", "Instalación profesional", "Sellado y terminaciones".
8. Acordeón de detalles con tres secciones (la primera abierta): "Características", "Cómo es la instalación" y "Preguntas frecuentes". Cada una con 2 a 3 líneas de texto de ejemplo.
9. "Productos relacionados": título y 3 Tarjetas de producto (por ejemplo "Ventana termopanel abatible", "Ventana de aluminio corredera" y "Ventana de PVC proyectante"), cada una con foto, nombre, etiqueta de material y botón secundario "Ver detalle".
10. Footer: igual que en la landing.
11. Botón flotante de WhatsApp.
```

### 4. Contacto

```text
Pantalla: Contacto de Construcciones Maibru, versión desktop. Usa el design system del proyecto.
Objetivo: Camila contacta rápido a la empresa por el medio que prefiera y comprueba que la empresa trabaja en su comuna. No hay formulario: todo el contacto es directo.
Componentes, de arriba hacia abajo:
1. Navbar: igual que en la landing, con "Contacto" marcado como página activa.
2. Encabezado de página: título h1 "Contáctanos" y texto "Cuéntanos qué necesitas y te respondemos a la brevedad. Cotizamos según las necesidades de cada proyecto."
3. Tres tarjetas de contacto en una fila, cada una con ícono grande, título, dato de contacto y botón:
   - WhatsApp: dato "+56 9 XXXX XXXX", texto "Respuesta rápida por mensaje" y botón principal "Escribir por WhatsApp".
   - Teléfono: dato "+56 9 XXXX XXXX", texto "Llámanos en horario de atención" y botón secundario "Llamar".
   - Correo: dato "contacto@ejemplo.cl", texto "Cuéntanos tu proyecto con detalle" y botón secundario "Enviar correo".
4. Bloque de horario de atención: "Lunes a viernes de 9:00 a 18:00 · Sábado de 9:00 a 13:00" (horario de ejemplo).
5. Bloque de cobertura, en dos columnas: a la izquierda el título "Dónde trabajamos", el texto "Atendemos la región de Valparaíso" y chips con las comunas (por ejemplo Valparaíso, Viña del Mar, Concón, Quilpué, Villa Alemana); a la derecha, un mapa simple de la zona.
6. Bloque "Antes de escribirnos": lista de 3 datos útiles que ayudan a cotizar más rápido: "Tipo de trabajo (ventanas, vidrio templado o remodelación)", "Comuna donde se realizará" y "Medidas aproximadas o fotos del lugar".
7. Redes sociales: título "Mira más trabajos en nuestras redes" y dos botones secundarios con ícono: "Instagram" y "Facebook".
8. Preguntas frecuentes: acordeón con 5 preguntas (la primera abierta): "¿Instalan las ventanas o solo las venden?", "¿Cómo pido un presupuesto?", "¿En qué comunas trabajan?", "¿Hacen remodelaciones de casas completas?" y "¿Qué materiales de ventana trabajan?". Cada respuesta de 2 líneas.
9. Footer: igual que en la landing.
10. Botón flotante de WhatsApp.
```

### 5. Blog

```text
Pantalla: Blog de Construcciones Maibru, versión desktop. Usa el design system del proyecto.
Objetivo: Camila encuentra artículos útiles para decidir qué ventana instalar o cómo planificar su remodelación, y desde ellos llega al catálogo o a WhatsApp.
Componentes, de arriba hacia abajo:
1. Navbar: igual que en la landing, con "Blog" marcado como página activa.
2. Encabezado de página: título h1 "Blog" y texto "Consejos para elegir, cuidar y renovar tu hogar."
3. Barra de búsqueda de artículos, con el texto de ayuda "Buscar artículos".
4. Chips de categoría en una fila: "Todos" (activo), "Proyectos de remodelación", "Diseño y aprovechamiento de espacios", "Guía de ventanas" y "Cuidado y mantención".
5. Artículo destacado, en dos columnas: imagen grande a la izquierda; a la derecha el chip "Guía de ventanas", el título "PVC, aluminio o termopanel: cuál conviene para tu casa", un extracto de 2 líneas, la fecha, el tiempo de lectura "6 min" y el botón principal "Leer artículo".
6. Cuadrícula de 6 Tarjetas de artículo, en dos filas de tres. Cada una con imagen, chip de categoría, título (máximo 3 líneas), fecha y enlace "Leer más". Los artículos son:
   - Proyectos de remodelación: "Claves para planificar la remodelación de tu casa sin sorpresas en el presupuesto".
   - Diseño y aprovechamiento de espacios: "5 tendencias en ventanas que aumentan el valor y la eficiencia energética de tu hogar".
   - Guía de ventanas: "Ventanas de PVC o de aluminio: diferencias que debes conocer".
   - Cuidado y mantención: "Cómo saber cuándo reemplazar tus ventanas y cómo cuidarlas".
   - Guía de ventanas: "Qué es el termopanel y cuándo conviene instalarlo".
   - Diseño y aprovechamiento de espacios: "Cierres de terraza con vidrio templado: ideas para ganar espacio".
7. Botón secundario centrado "Ver más artículos".
8. Estado sin resultados (variante pequeña): mensaje "No encontramos artículos con esa búsqueda" y botón secundario "Ver todos los artículos".
9. Llamado a la acción: título "¿Tienes un proyecto en mente?", texto "Cuéntanos qué necesitas y te asesoramos." y botón principal "Escribir por WhatsApp".
10. Footer: igual que en la landing.
11. Botón flotante de WhatsApp.
```

### 6. Artículo

```text
Pantalla: Artículo del blog de Construcciones Maibru, versión desktop. Usa el design system del proyecto.
Objetivo: Camila lee un artículo útil para decidir qué ventana instalar, lo comparte o comenta, y pasa al catálogo o a WhatsApp.
Componentes, de arriba hacia abajo:
1. Navbar: igual que en la landing, con "Blog" marcado como página activa.
2. Migas de pan: Inicio > Blog > PVC, aluminio o termopanel: cuál conviene para tu casa.
3. Encabezado del artículo: chip "Guía de ventanas", título h1 "PVC, aluminio o termopanel: cuál conviene para tu casa", y una línea con la fecha, el tiempo de lectura "6 min" y el autor "Construcciones Maibru".
4. Imagen destacada del artículo, a ancho de contenido.
5. Cuerpo del artículo, en una columna de lectura de máximo 70 caracteres por línea, con una introducción de 3 líneas y estos subtítulos h2, cada uno con 2 párrafos cortos:
   - "¿Qué diferencia hay entre PVC, aluminio y termopanel?"
   - "Aislación térmica y acústica"
   - "Mantención y durabilidad"
   - "Cuál elegir según tu caso"
6. Tabla comparativa dentro del artículo, con columnas "PVC", "Aluminio" y "Termopanel" y filas "Aislación", "Mantención" e "Ideal para", con una frase corta en cada celda.
7. Botones de compartir: "Facebook", "WhatsApp" y "Copiar enlace". Al copiar el enlace aparece el mensaje "Enlace copiado".
8. Llamado a la acción: título "¿Quieres cambiar tus ventanas?", texto "Mira nuestro catálogo o escríbenos y te asesoramos.", botón secundario "Ver catálogo" y botón principal "Escribir por WhatsApp".
9. Comentarios: título "Comentarios (2)", formulario con campos "Nombre" y "Comentario" y botón principal "Publicar comentario", y debajo 2 comentarios de ejemplo, cada uno con nombre, fecha y texto de 2 líneas, marcados como "Ejemplo".
10. Artículos relacionados: título y 3 Tarjetas de artículo.
11. Footer: igual que en la landing.
12. Botón flotante de WhatsApp.
```

### Versión mobile (para cada pantalla)

```text
Genera la versión mobile (375px de ancho) de esta pantalla siguiendo la
sección Layout del design system:
- El menú del Navbar se convierte en un botón de menú (hamburguesa), con el logo a la izquierda y el botón "Contáctanos" dentro del menú desplegable.
- Todo el contenido va en una sola columna, con márgenes laterales de 16 px y los botones a ancho completo.
- Las cuadrículas de tarjetas pasan a una columna, y las filas de chips se deslizan horizontalmente.
- En la ficha de producto, la galería va arriba y la información debajo; los botones "Llamar" y "Enviar correo" quedan lado a lado.
- En el artículo, la tabla comparativa se desliza horizontalmente dentro de su contenedor.
- Usa los tamaños de título para celular (h1 de 32 px, h2 de 28 px, h3 de 20 px).
- El Botón flotante de WhatsApp se mantiene fijo en la esquina inferior derecha y no tapa los botones.
- El texto no baja de 16 px y los botones tienen un alto mínimo de 44 px.
```
