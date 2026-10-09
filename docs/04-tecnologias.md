# Tecnologías del proyecto — Construcciones Maibru

> Guía: [Tecnologías del proyecto](../evaluacion/guias/fase-1-requerimientos/04-tecnologias.md)

## Stack

| Área | Herramienta | Para qué la uso |
|---|---|---|
| Construcción | HTML + CSS | Maquetar la estructura semántica y aplicar los estilos visuales del sitio web sin dependencias de frameworks ni CMS. |
| Versionado | Git y GitHub | Llevar el control de versiones, registrar el avance mediante commits y respaldar el código del proyecto en la nube. |
| Publicación | GitHub Pages | Alojar y desplegar el sitio web estático de forma gratuita mediante una URL pública accesible. |
| Diseño | Whimsical | Crear wireframes, arquitectura de información, moodboard y estructuración visual de los componentes. |
| Diseño | Google Stitch | Generar prototipos visuales en alta fidelidad a partir de las especificaciones y tokens de diseño. |
| IA | Antigravity / Gemini | Asistir en la estructuración de documentos de requerimientos, redacción de contenidos y soporte de código. |
| Editor | Antigravity IDE | Escribir, organizar y editar el código fuente del proyecto con asistencia inteligente integrada. |

## Qué es funcional y qué es prototipo

| Funcionalidad | Estado en esta versión |
|---|---|
| Navegación entre páginas y secciones (Inicio, Servicios, Galería, Sobre nosotros, Contacto) | Funcional |
| Visualización del catálogo de servicios y tipos de ventanas (PVC, Termopanel, Aluminio) | Funcional |
| Galería de fotografías de proyectos y obras realizadas | Funcional |
| Botón de contacto directo a WhatsApp (`wa.me`) con mensaje predefinido | Funcional |
| Enlaces directos a redes sociales y llamadas telefónicas (`tel:`, `mailto:`) | Funcional |
| Visualización de información institucional y comunas de cobertura (V Región) | Funcional |
| Sección de testimonios y referencias de clientes | Funcional |
| Formulario de solicitud de cotización (comuna, tipo de obra, medidas y contacto) | Prototipo visual |

## Integraciones para una versión real

- **Procesamiento de Formularios (Formspree / EmailJS):** Para recibir las solicitudes de cotización directamente en el correo electrónico del emprendimiento sin necesidad de un servidor complejo.
- **Enlace directo a WhatsApp personal / Business:** Para que el cliente inicie la conversación directamente con el número de WhatsApp del negocio, facilitando la atención directa sin requerir APIs complejas. 
- **Google Maps API:** Mapa interactivo que muestre de forma visual el radio de cobertura y comunas atendidas en la Región de Valparaíso.
- **Google Analytics:** Para medir el tráfico de usuarios, páginas más visitadas y la tasa de conversión en clics de contacto.

## Restricciones

- **Plazo:** Proyecto correspondiente a la evaluación académica del semestre (desarrollo dividido en Fase 1: Requerimientos, Fase 2: Specs y Fase 3: Prototipo).
- **Marca:** No existe un manual de identidad corporativa formal previo; los colores corporativos, tipografía y estilo visual se definen en la Fase 2 enfocados en proyectar confianza y profesionalismo en el rubro de la construcción.
- **Dispositivos:** Diseño completamente responsivo (Mobile-First y Desktop), dando máxima prioridad a teléfonos móviles, ya que la proto-persona (Camila) busca servicios y cotiza principalmente desde su smartphone.
- **Técnicas:** Uso de HTML5, CSS3 y JavaScript básico, sin frameworks pesados ni bases de datos dinámicas, asegurando alta velocidad de carga y total compatibilidad con GitHub Pages.
- **Pagos (Transferencia Bancaria o efectivo):** Para facilitar el pago de anticipos de materiales o el cobro de visitas técnicas de evaluación en terreno.
