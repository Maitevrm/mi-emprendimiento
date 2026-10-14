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
Objetivo: Camila entiende en pocos segundos qué ofrece la empresa, ve trabajos reales y contacta por WhatsApp.
Componentes, de arriba hacia abajo:
1. Navbar: logo de Construcciones Maibru a la izquierda, menú (Inicio, Servicios, Catálogo, Proyectos, Blog, Contacto) y botón principal "Contáctanos".
2. Hero: foto de fondo de un trabajo real con capa oscura, título "Ventanas y remodelaciones en un solo lugar", texto "Producto, instalación de ventanas y remodelación de viviendas en la región de Valparaíso.", botón principal "Pedir presupuesto por WhatsApp" y botón secundario "Ver proyectos".
3. Tarjeta de servicio (3): "Ventanas" (PVC, termopanel y aluminio con instalación incluida), "Vidrio templado" (cierres de terraza, shower door y divisiones), "Remodelaciones" (desde una pieza hasta la casa completa).
4. Bloque de confianza (3): "Producto e instalación", "Atención directa" y "Presupuesto a medida", cada uno con una frase corta.
5. Galería de proyectos: sección "Portafolio de proyectos" sobre fondo blanco limpio, con título centrado. Muestra una cuadrícula de 6 tarjetas de proyecto dispuestas en dos filas de tres (3x2). Cada tarjeta tiene esquinas redondeadas (8 px), una fotografía de alta calidad de un trabajo de construcción o instalación en la parte superior y una superposición de degradado oscuro en la parte inferior que contiene el texto. El texto sigue un formato estricto: en la primera línea el nombre del proyecto en letra blanca y negrita (Montserrat Bold), y en la segunda línea la ubicación en verde vivo (#66C21A). Ejemplo de tarjeta: "Cierre de terraza en vidrio templado" y debajo "Viña del Mar".
6. Tarjeta de experiencia (3): nombre del cliente, tipo de trabajo y opinión breve.
7. Tarjeta de artículo (3): imagen, categoría, título y enlace "Leer más".
8. Footer: logo, teléfono, WhatsApp, correo, comunas de cobertura de la región de Valparaíso y enlaces a Instagram y Facebook.
9. Botón flotante de WhatsApp fijo en la esquina inferior derecha.
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
Pantalla: Blog de [nombre], versión desktop. Usa el design system del proyecto.
Objetivo: 
Componentes, de arriba hacia abajo:
1. Navbar.
2. 
```

### 6. Artículo

```text
Pantalla: Artículo del blog de [nombre], versión desktop. Usa el design system del proyecto.
Objetivo: 
Componentes, de arriba hacia abajo:
1. Navbar.
2. 
```

### Versión mobile (para cada pantalla)

```text
Genera la versión mobile (375px de ancho) de esta pantalla siguiendo la
sección Layout del design system: 
```
