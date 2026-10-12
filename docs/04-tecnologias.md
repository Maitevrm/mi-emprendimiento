# Tecnologías del proyecto — Construcciones Maibru SpA

> Guía: [Tecnologías del proyecto](../evaluacion/guias/fase-1-requerimientos/04-tecnologias.md)

## Stack

| Área | Herramienta | Para qué la uso |
|---|---|---|
| Construcción | HTML + CSS | Maquetar la estructura semántica y aplicar los estilos visuales del sitio web sin dependencias de frameworks ni CMS. |
| Versionado | Git y GitHub | Llevar el control de versiones, registrar el avance mediante commits y respaldar el código del proyecto en la nube. |
| Publicación | GitHub Pages | Alojar y desplegar el sitio web estático de forma gratuita mediante una URL pública accesible. |
| Diseño | Whimsical | Crear wireframes, arquitectura de información, moodboard y estructuración visual de los componentes. |
| Diseño | Google Stitch | Generar prototipos visuales en alta fidelidad a partir de las especificaciones y tokens de diseño. |
| IA | Antigravity / Claude | Asistir en la estructuración de documentos de requerimientos, redacción de contenidos y soporte de código. |
| Editor | Antigravity IDE | Escribir, organizar y editar el código fuente del proyecto con asistencia inteligente integrada. |

## Qué es funcional y qué es prototipo

| Funcionalidad | Estado en esta versión |
|---|---|
| Navegación entre páginas y secciones (Inicio, Servicios, Catálogo, Galería, Blog, Sobre nosotros, Contacto) | Funcional |
| Visualización del catálogo de servicios y tipos de ventanas (PVC, termopanel, aluminio, vidrio templado) | Funcional |
| Búsqueda y filtro del catálogo por categoría (material o tipo de apertura) | Prototipo visual |
| Galería de fotografías de proyectos y obras realizadas | Funcional |
| Botón de contacto directo a WhatsApp (`wa.me`) con mensaje predefinido | Funcional |
| Consulta por una ventana específica por WhatsApp, con el producto mencionado en el mensaje | Funcional |
| Enlaces directos a Instagram y Facebook, llamadas telefónicas (`tel:`) y correo (`mailto:`) | Funcional |
| Visualización de información institucional y comunas de cobertura (V Región) | Funcional |
| Visualización de experiencias de clientes | Funcional |
| Formulario para dejar una experiencia nueva | Prototipo visual |
| Lectura de artículos del blog | Funcional |
| Navegación del blog por categorías | Prototipo visual |
| Comentar artículos | Prototipo visual |
| Compartir artículos en redes sociales | Prototipo visual |

## Integraciones para una versión real

- **Enlace directo a WhatsApp personal / Business:** Para que el cliente inicie la conversación directamente con el número de WhatsApp del negocio, facilitando la atención directa sin requerir APIs complejas.
- **Google Maps API:** Mapa interactivo que muestre de forma visual el radio de cobertura y comunas atendidas en la Región de Valparaíso. 
- **Google Analytics:** Para medir el tráfico de usuarios, páginas más visitadas y la tasa de conversión en clics de contacto.
- **Servicio de recepción de experiencias (por ejemplo Formspree) con moderación:** Para que los clientes envíen su experiencia y el dueño la revise y la publique, evitando mensajes ofensivos o spam. Se podría complementar con un enlace a las reseñas de Google de la empresa.
- **Instagram y Facebook (plugins de página):** Para mostrar en el sitio las publicaciones recientes y las recomendaciones de las páginas de la empresa, sin tener que actualizarlas dos veces.

## Restricciones

- **Plazo:** Proyecto correspondiente a la evaluación académica del semestre (desarrollo dividido en Fase 1: Requerimientos, Fase 2: Specs y Fase 3: Prototipo).
- **Marca:** No existe un manual de identidad corporativa formal previo; los colores corporativos, tipografía y estilo visual se definen en la Fase 2 enfocados en proyectar confianza y profesionalismo en el rubro de la construcción.
- **Dispositivos:** Diseño completamente responsivo (Mobile-First y Desktop), dando máxima prioridad a teléfonos móviles, ya que la proto-persona (Camila) busca servicios y contacta principalmente desde su smartphone.
- **Técnicas:** Uso de HTML5, CSS3 y JavaScript básico, sin frameworks pesados ni bases de datos dinámicas, asegurando alta velocidad de carga y total compatibilidad con GitHub Pages.
- **Alcance del prototipo:** El sitio no procesa cotizaciones ni pagos. Todo el contacto se realiza de forma directa por WhatsApp, teléfono o correo electrónico. Los comentarios del blog son solo visuales en esta versión.