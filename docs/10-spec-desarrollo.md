# Spec de desarrollo — Andjelica Braids Studio

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio de Andjelica Braids Studio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML5 semántico y CSS3 puro (sin frameworks externos ni Tailwind), la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

---

## 1. Estructura de archivos

```text
andjelica-braids/
├── index.html                  ← Landing page y presentación del estudio
├── tienda.html                 ← Catálogo de insumos y servicios con filtros
├── producto.html               ← Ficha de detalle de producto con guía de uso
├── carrito.html                ← Carrito de compras con cálculo de despacho
├── blog.html                   ← Catálogo de artículos con filtros por categorías
├── articulo.html               ← Artículo educativo individual con comentarios
├── contacto.html               ← Formulario de contacto y agendamiento
├── sobre-mi.html               ← Historia de la trenzadora y filosofía de cuidado
├── preguntas-frecuentes.html   ← Preguntas frecuentes (FAQ de dolor, tiempos y envíos)
├── terminos.html               ← Términos, condiciones y políticas de abono
├── privacidad.html             ← Política de privacidad y tratamiento de datos
├── 404.html                    ← Página de error personalizada
├── DESIGN.md                   ← Design system oficial del proyecto
├── css/
│   ├── styles.css              ← Estilos globales, variables :root y componentes
│   └── reset.css               ← Reseteo de estilos base estándar
├── img/
│   ├── logo.svg
│   ├── hero/
│   ├── productos/
│   ├── blog/
│   └── clientas/
├── stitch/                     ← Código exportado de Stitch (referencia visual)
└── docs/                       ← Documentación y especificaciones del proyecto
```

---

## 2. Páginas y navegación

- **Navbar persistente en todas las páginas:** Logotipo con enlace a `index.html`, menú de enlaces (`index.html`, `tienda.html`, `blog.html`, `sobre-mi.html`, `contacto.html`), buscador, botón "Agendar Cita" con enlace directo a `contacto.html` (o WhatsApp) e ícono de carrito que dirige a `carrito.html` con contador dinámico.
- **Footer en todas las páginas:** Enlaces informativos a `sobre-mi.html`, `contacto.html`, `preguntas-frecuentes.html`, `terminos.html`, `privacidad.html`, redes sociales (@andjelicabraids) y ubicación en Valparaíso.

| Desde | Elemento interactivo | Lleva a |
|---|---|---|
| `index.html` | Botón "Cotizar y Agendar Peinado" (Hero) | `contacto.html` / `service-calculator` |
| `index.html` | Botón "Ver Tienda e Insumos" (Hero) | `tienda.html` |
| `index.html` | Botón "Reservar este Estilo por WhatsApp" (Cotizador) | `https://wa.me/569XXXXXXXX?text=Hola%20Andjelica,%20quiero%20agendar%20Knotless%20Braids` |
| `index.html` | Botón "Ver Producto" (Card destacada) | `producto.html` |
| `index.html` | Formulario de leads "Obtener Guía y Descuento" | Confirmación visual + lead captado |
| `tienda.html` | Chips de categorías / Filtros | Filtra la grilla de productos en la misma página |
| `tienda.html` | Botón "Ver Detalle" de cualquier `card-product` | `producto.html` |
| `producto.html` | Botón "Agregar al Carrito" | `carrito.html` |
| `producto.html` | Botón "Consultar por WhatsApp" | `https://wa.me/569XXXXXXXX?text=Hola,%20tengo%20una%20duda%20sobre%20el%20Mousse` |
| `producto.html` | Tarjeta de producto complementario | `producto.html` (otro producto) |
| `carrito.html` | Selector de comuna / Botón calcular | Actualiza total en `carrito.html` |
| `carrito.html` | Botón "← Seguir comprando" | `tienda.html` |
| `carrito.html` | Botón "Proceder al Pago Seguro" | Simulación de checkout / Pasarela |
| `blog.html` | Chips de categorías del blog | Filtra artículos en `blog.html` |
| `blog.html` | Card o Banner "Leer Guía Completa" | `articulo.html` |
| `articulo.html` | Card de producto recomendado ("Mousse con Argán") | `producto.html` |
| `articulo.html` | Botones "Compartir en WhatsApp / Redes" | Enlace nativo de compartir (`whatsapp://send...`) |
| `articulo.html` | Formulario "Publicar Comentario" | Inserción de nuevo comentario en la página |
| `404.html` | Botón "Volver al Inicio" | `index.html` |

---

## 3. Estructura semántica

### `index.html` (Landing Page)
```html
<header>
  <nav class="navbar"> <!-- logo, menú navegación, buscador, botón agendar, carrito --> </nav>
</header>
<main>
  <section class="hero"> <!-- texto, CTA buttons, badge sin dolor, foto editorial --> </section>
  <section class="benefits"> <!-- 3 columnas de beneficios clave --> </section>
  <section class="service-calculator"> <!-- cotizador interactivo de estilos y largo --> </section>
  <section class="featured-products"> <!-- grilla de 3 productos destacados --> </section>
  <section class="testimonials"> <!-- reseñas y fotos reales de clientas --> </section>
  <section class="lead-magnet"> <!-- formulario de descarga de guía y cupón 10% --> </section>
</main>
<footer class="footer"> <!-- 4 columnas con datos, links legales y redes --> </footer>
```

### `tienda.html` (Tienda de Insumos)
```html
<header> <nav class="navbar"></nav> </header>
<main class="store-layout">
  <section class="store-header"> <!-- título, buscador principal y chips de categorías --> </section>
  <div class="store-container">
    <aside class="store-filters"> <!-- filtros por uso, precio y stock --> </aside>
    <section class="products-grid">
      <!-- Múltiples elementos <article class="product-card"> con imágenes, precio y botón -->
    </section>
  </div>
</main>
<footer class="footer"></footer>
```

### `producto.html` (Ficha de Producto)
```html
<header> <nav class="navbar"></nav> </header>
<main class="product-detail">
  <nav class="breadcrumbs" aria-label="Migas de pan"></nav>
  <section class="product-hero">
    <div class="product-gallery"> <!-- imagen principal y miniaturas --> </div>
    <div class="product-info"> <!-- título, precio, variantes, selector cantidad, botón agregar --> </div>
  </section>
  <section class="product-tabs"> <!-- modo de uso, ingredientes y FAQs --> </section>
  <section class="related-products"> <!-- productos complementarios --> </section>
</main>
<footer class="footer"></footer>
```

### `carrito.html` (Carrito de Compras)
```html
<header> <nav class="navbar"></nav> </header>
<main class="cart-layout">
  <section class="cart-items"> <!-- tabla/lista de artículos con miniaturas y cantidades --> </section>
  <aside class="cart-summary"> <!-- subtotal, calculadora de despacho, cupón y total --> </aside>
</main>
<footer class="footer"></footer>
```

### `blog.html` y `articulo.html`
```html
<header> <nav class="navbar"></nav> </header>
<main class="article-layout">
  <article class="single-post">
    <header class="post-header"> <!-- categoría, título h1, autor, tiempo lectura --> </header>
    <figure class="post-featured-image"> <img alt="..."> </figure>
    <div class="post-content">
      <!-- Párrafos, encabezados h2, bloque de producto recomendado <aside class="product-callout"> -->
    </div>
    <footer class="post-footer"> <!-- botones para compartir y formulario de comentarios --> </footer>
  </article>
</main>
<footer class="footer"></footer>
```

---

## 4. Organización del CSS

```css
/* ==========================================================================
   VARIABLES Y DESIGN TOKENS (Sincronizados con DESIGN.md)
   ========================================================================== */
:root {
  /* Colores */
  --color-primary: #7B341E;
  --color-primary-hover: #5E2713;
  --color-on-primary: #FFFFFF;
  --color-secondary: #F5EBE1;
  --color-on-secondary: #2B1D16;
  --color-tertiary: #C87D20;
  --color-tertiary-strong: #8E4506;
  --color-on-tertiary: #FFFFFF;
  --color-bg: #FDFBF7;
  --color-surface: #FFFFFF;
  --color-text: #2B1D16;
  --color-text-soft: #6E5D53;
  --color-outline: #E5D9CE;
  --color-disabled: #E2DDD8;
  --color-on-disabled: #8C837C;
  --color-error: #BA1A1A;
  --color-success: #1E6B24;

  /* Tipografías */
  --font-title: 'Outfit', sans-serif;
  --font-body: 'Plus Jakarta Sans', sans-serif;

  /* Escala Tipográfica */
  --font-size-display: 3rem;     /* 48px */
  --font-size-h2: 2rem;          /* 32px */
  --font-size-h3: 1.375rem;      /* 22px */
  --font-size-body: 1rem;        /* 16px */
  --font-size-sm: 0.875rem;      /* 14px */
  --font-size-btn: 0.9375rem;    /* 15px */

  /* Espaciados */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios de borde */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-pill: 9999px;

  /* Sombras y elevaciones */
  --shadow-sm: 0 4px 16px rgba(123, 52, 30, 0.06);
  --shadow-md: 0 10px 24px rgba(123, 52, 30, 0.12);
  --shadow-lg: 0 12px 32px rgba(43, 29, 22, 0.16);
}
```

- **Convención de nomenclatura:** Nombres de clases en inglés en formato kebab-case (`.navbar`, `.hero-section`, `.btn-primary`, `.product-card`, `.price-tag`).
- **Estrategia Mobile-First:** Se escriben los estilos móviles por defecto y se amplían mediante `@media (min-width: 768px)` (tablet) y `@media (min-width: 1024px)` (desktop).
- **Contenedor:** `.container { max-width: 1200px; margin: 0 auto; padding: 0 16px; }`.

---

## 5. Criterios de aceptación

### Navegación y Flujos
- [ ] La barra de navegación y el footer son consistentes e idénticos en las 6 páginas principales y páginas secundarias.
- [ ] Se puede completar el **Flujo 1 de compra / reserva**: Landing → Tienda → Ficha de Producto con selección de variante → Carrito → Cálculo de despacho.
- [ ] Se puede completar el **Flujo 2 de contenido**: Blog → Lectura de Artículo → Clic en Producto Recomendado → Ficha de Producto.
- [ ] No existen enlaces rotos ni botones sin destino funcional.

### Funcionalidades
- [ ] La landing page incluye el formulario de captación de leads con mensaje de confirmación de guía descargable y 10% de descuento.
- [ ] La landing page incluye el cotizador interactivo de estilos y largos de trenzas.
- [ ] La tienda cuenta con buscador funcional, chips de categorías y filtros por uso y rango de precios.
- [ ] La ficha de producto incluye selector de formato/presentación, cantidad, pestañas de modo de uso e ingredientes, y botón de consulta directa por WhatsApp.
- [ ] El carrito de compras permite simular el costo de despacho según la comuna seleccionada y aplicar cupones de descuento.
- [ ] Los artículos del blog tienen botones funcionales para compartir en redes sociales y formulario para ingresar comentarios.

### Diseño e Identidad Visual
- [ ] Todos los colores y fuentes provienen rigurosamente de las variables `:root` definidas en `DESIGN.md`.
- [ ] El contraste de texto sobre fondos cumple con el estándar WCAG AA (mínimo 4.5:1).
- [ ] Los precios en pesos chilenos (`$XX.XXX CLP`) son siempre visibles en todas las tarjetas de producto sin necesidad de interacción previa.
- [ ] Todos los botones y tarjetas poseen estados visuales de `:hover`, `:active` y `:focus-visible`.

### Responsive y Adaptabilidad Móvil
- [ ] En pantallas móviles (375px) no existe ningún desbordamiento ni scroll horizontal.
- [ ] En pantallas móviles la grilla de productos se reorganiza a 1 columna (o cuadrícula táctil) y el menú superior se adapta a formato móvil.
- [ ] Todos los elementos interactivos y botones en versión móvil tienen un área táctil mínima de 48px de alto.

### Accesibilidad, Semántica y Publicación
- [ ] Todas las imágenes poseen atributo `alt` descriptivo.
- [ ] Cada página web contiene un único encabezado principal `<h1>` estructurado jerárquicamente con `<h2>` y `<h3>`.
- [ ] El código HTML5 es 100% válido y semántico (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`).
- [ ] El proyecto está alojado y publicado correctamente en GitHub Pages.
