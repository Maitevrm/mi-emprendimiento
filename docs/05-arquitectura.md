# Arquitectura de la información — [Nombre del emprendimiento]

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

<!-- Incluye landing, blog, tienda y las páginas obligatorias:
contacto, preguntas frecuentes, términos, privacidad y 404. -->

```text
Inicio (landing)
├── Servicios
│   ├── Remodelaciones de viviendas
│   └── Instalación y reemplazo profesional
├── Catálogo
│   ├── Ventanas de termopanel, PVC y aluminio (filtro por material o tipo de apertura)
│   ├── Cierres de cristal y vidrio templado
│   └── Ficha de producto
├── Galería de trabajos
├── Experiencias de clientes
├── Blog
│   ├── Proyectos de remodelación
│   ├── Diseño y aprovechamiento de espacios
│   ├── Guía de ventanas
│   ├── Cuidado y mantención
│   └── Artículo
├── Sobre nosotros (empresa y comunas de cobertura)
├── Contacto
├── Preguntas frecuentes
├── Términos y condiciones
├── Política de privacidad
└── Página 404
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

```text
Como el sitio no tiene carrito ni cotizador, el flujo termina cuando Camila contacta a la empresa por WhatsApp con la ventana que le interesa.

```
Instagram o Google → Inicio → [Ver ventanas] → Catálogo → Categoría "Ventanas de termopanel, PVC y aluminio" → Filtro "PVC"
→ Ficha de producto → [Consultar por WhatsApp] → WhatsApp con mensaje predefinido

```

### Flujo 2: contenido

```text
Camila llega buscando información y termina contactando a la empresa.

```
Google ("ventanas termopanel ahorro") → Blog → Artículo "PVC, aluminio o termopanel: cuál conviene para tu casa"
→ [Ver ventanas de termopanel, PVC y aluminio] → Ficha de producto → [Consultar por WhatsApp]

```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

| Categoría | Productos |
|---|---|
| Ventanas de Termopanel, PVC y Aluminio | Ventanas de termopanel en PVC (aislación térmica/acústica), Ventanas correderas/abatibles de aluminio, Ventanales a medida. |
| Cierres de Cristal y Vidrio Templado | Cierres de terraza con cristal templado, Shower door de vidrio templado, Divisiones de ambientes en cristal. |
| Remodelaciones de Viviendas | Remodelación completa de casas, Ampliaciones, Cocinas y baños, Pisos y revestimientos, Terminaciones y obras menores. |
| Instalación y Reemplazo Profesional | Servicio de retiro e instalación de ventanas viejas, Mantención y sellado de ventanales, Montaje e instalación de estructuras. |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
|---|---|---|---|
| Proyectos de Remodelación | Claves para planificar la remodelación de tu casa sin sorpresas en el presupuesto | Quiere renovar su hogar, pero le preocupa la logística, los tiempos y los costos. | Remodelaciones de Viviendas. |
| Diseño y Aprovechamiento de Espacios | 5 tendencias en ventanas que aumentan el valor y la eficiencia energética de tu hogar | Quiere que su casa se vea mejor y gaste menos en calefacción, pero no sabe qué opciones existen. | Ventanas de Termopanel, PVC y Aluminio. |
| Guía de Ventanas | PVC, aluminio o termopanel: cuál conviene para tu casa | Necesita decidir qué tipo de ventana instalar antes de contactar a una empresa. | Ventanas de Termopanel, PVC y Aluminio. |
| Cuidado y Mantención | Cómo saber cuándo reemplazar tus ventanas y cómo cuidarlas | Quiere alargar la vida útil de sus ventanas y evitar problemas de filtraciones o ruido. | Instalación y Reemplazo Profesional. |
