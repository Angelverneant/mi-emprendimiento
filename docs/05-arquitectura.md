# Arquitectura de la información — Andjelica Braids Studio

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

```text
Inicio (Landing Page)
├── Servicios y Tienda (Catálogo de peinados e insumos)
│   ├── Categoría: Extensiones de Kanekalon
│   ├── Categoría: Cuidado y Fijación Capilar
│   ├── Categoría: Accesorios y Satén
│   ├── Ficha de Producto / Servicio (con guía de preparación y cuidados)
│   └── Carrito de Compras (con simulador de despacho)
├── Blog (Consejos y Tendencias)
│   ├── Categoría: Cuidados y Mantenimiento
│   ├── Categoría: Estilos y Tendencias
│   ├── Categoría: Salud Capilar y Transición
│   └── Artículo del Blog (con productos relacionados y comentarios)
├── Sobre Mí (Historia de la trenzadora y filosofía)
├── Contacto y Citas (Formulario y enlace a WhatsApp)
├── Preguntas Frecuentes (FAQ - tiempos, dolor, cuidados, envíos)
├── Términos y Condiciones (Políticas de abono, cancelaciones y garantías)
├── Política de Privacidad (Tratamiento de datos personales y correos)
└── Página 404 (Página de error amigable con botón de retorno al inicio)
```

---

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: Compra de insumos / Reserva de peinado

```text
Instagram (Reel de transformación con Knotless Braids)
→ Landing Page
→ [Hace clic en "Ver Tienda e Insumos"]
→ Tienda y Catálogo
→ [Filtra por categoría "Cuidado y Fijación" y busca "Mousse"]
→ Ficha de producto: "Mousse Fijador Anti-Frizz con Aceite de Argán"
→ [Lee beneficios, modo de uso y selecciona presentación de 250ml]
◇ ¿Desea agendar servicio de trenzas además del producto?
   ├── Sí → [Hace clic en "Cotizar Peinado por WhatsApp"] → WhatsApp con trenzadora
   └── No → [Hace clic en "Agregar al carrito"]
→ Carrito de Compras
→ [Ingresa su comuna para calcular costo de despacho]
→ Fin: Carrito listo para proceder al pago
```

### Flujo 2: Contenido educativo y conversión

```text
TikTok / Google ("cómo lavar el pelo con trenzas africanas sin desarmarlas")
→ Artículo del Blog: "Guía paso a paso: Cómo lavar y secar tus trenzas sin generar frizz"
→ [Lee la guía y encuentra recomendación del gorro de satén y aceite para cuero cabelludo]
→ [Hace clic en el producto recomendado: "Gorro de Satén Doble Capa"]
→ Ficha de producto: "Gorro de Satén Premium"
◇ ¿Desea comprar en el momento?
   ├── Sí → [Agrega al carrito] → Carrito de compras
   └── No → [Regresa al artículo y completa el formulario de suscripción para recibir la Guía en PDF y el cupón de 10% de descuento]
          → Fin: Lead captado exitosamente
```

---

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos e insumos

| Categoría | Productos |
|---|---|
| **Extensiones de Kanekalon** | Kanekalon Jumbo liso (colores naturales 1B, 2, 4), Kanekalon Ombré bitono/tritono, Pelo rizado para French Curls y Goddess Braids |
| **Cuidado y Fijación** | Gel fijador de bordes (Edge Control extra fuerte sin escamas), Mousse fijador espumoso anti-frizz, Aceite hidratante de romero y menta para cuero cabelludo, Spray calmante anti-picazón |
| **Accesorios y Satén** | Gorros de satén ajustables de doble capa, Fundas de almohada de satén, Anillos y puños decorativos dorados/plateados para trenzas, Bandas elásticas suaves |

*Filtros adicionales en la tienda:* Rango de precio, Tipo de uso (Durante el peinado / Mantenimiento diario) y Disponibilidad inmediata.

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de Valeria | Producto relacionado |
|---|---|---|---|
| **Cuidados y Mantenimiento** | *"Cómo lavar y secar tus trenzas paso a paso sin arruinar el peinado"* | Evitar el mal olor, picazón y acumulación de residuos en el cuero cabelludo | Mousse fijador anti-frizz y Spray calmante |
| **Estilos y Tendencias** | *"Knotless vs. Box Braids tradicionales: ¿cuál es la mejor opción para tu cabello?"* | Conocer la técnica que menos dolor produce y mejor cuida la raíz | Kanekalon premium y Servicio de Knotless Braids |
| **Salud Capilar y Transición** | *"Cómo preparar tu cabello natural antes de tu cita de trenzado"* | Proteger su hebra capilar para que no se quiebre ni sufra tracción | Aceite nutritivo de romero y Gorro de satén |
