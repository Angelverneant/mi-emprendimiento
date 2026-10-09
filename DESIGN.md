---
version: alpha
name: "Andjelica Braids Studio"
description: "Design system para Andjelica Braids Studio — Salón boutique de trenzado profesional e insumos capilares"
colors:
  primary: "#7B341E"
  primary-hover: "#5E2713"
  on-primary: "#FFFFFF"
  secondary: "#F5EBE1"
  on-secondary: "#2B1D16"
  tertiary: "#C87D20"
  tertiary-strong: "#8E4506"
  on-tertiary: "#FFFFFF"
  neutral: "#FDFBF7"
  surface: "#FFFFFF"
  on-surface: "#2B1D16"
  on-surface-variant: "#6E5D53"
  outline: "#E5D9CE"
  disabled: "#E2DDD8"
  on-disabled: "#8C837C"
  error: "#BA1A1A"
  on-error: "#FFFFFF"
  success: "#1E6B24"
  on-success: "#FFFFFF"
typography:
  headline-display:
    fontFamily: Outfit
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.1
  headline-lg:
    fontFamily: Outfit
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: Outfit
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  title-md:
    fontFamily: Outfit
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.3
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 15px
    fontWeight: 600
    lineHeight: 1
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1
rounded:
  sm: 4px
  md: 8px
  lg: 16px
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
    padding: 14px 28px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 14px 28px
  button-secondary-hover:
    backgroundColor: "{colors.outline}"
    textColor: "{colors.primary-hover}"
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
  card-article:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg}"
  tag-offer:
    backgroundColor: "{colors.tertiary-strong}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 4px 12px
  tag-category:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 14px
  tag-category-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 6px 14px
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 16px
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
    typography: "{typography.body-sm}"
  message-success:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.success}"
    typography: "{typography.body-sm}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

# Andjelica Braids Studio — Design System

## Overview

**Andjelica Braids Studio** es un salón boutique de trenzado profesional y venta de insumos capilares ubicado en Valparaíso, Chile. 

El diseño está concebido para **Valeria Méndez** (nuestra proto-persona principal), una joven creadora de contenido que busca servicios de trenzado impecables sin dolor y la conveniencia de adquirir insumos especializados en un sitio confiable, claro y transparente.

La interfaz transmite una estética **afro-chic, cálida, sofisticada, protectora y vital**, destacando el cuidado y la salud capilar mediante contrastes cálidos, microinteracciones suaves y tipografías estilizadas.

## Colors

- **Primary (`#7B341E` — Cacao Tostado):** Color principal de la marca. Se utiliza en el logotipo, botones primarios de acción (CTA), encabezados destacados y estados activos principales. *No usar como color de fondo general de páginas para no saturar la lectura.*
- **Primary Hover (`#5E2713` — Cacao Profundo):** Estado interactivo hover y active para botones y enlaces primarios.
- **Secondary (`#F5EBE1` — Arena Suave):** Color de apoyo para fondos de tarjetas de producto, bloques de testimonios, badges de categoría en reposo y filas alternadas.
- **Tertiary (`#C87D20` — Ámbar Dorado):** Color de acento para íconos decorativos, estrellas de calificación de 5 estrellas y bordes interactivos.
- **Tertiary Strong (`#8E4506` — Ámbar Intenso):** Fondo exclusivo para etiquetas con texto blanco (badges de oferta, descuentos, etiqueta "100% Sin dolor") asegurando contraste accesible WCAG AA (> 5.7:1).
- **Neutral (`#FDFBF7` — Crema Marfil):** Fondo general de todo el sitio web. Evita la frialdad del blanco puro y otorga una atmósfera acogedora.
- **Surface (`#FFFFFF` — Blanco Puro):** Fondo para campos de entrada de datos, menús desplegables, tarjetas elevadas del blog y ventanas modales.
- **On-Surface (`#2B1D16` — Espresso Oscuro):** Color estándar para textos de párrafos, títulos y números de precios.
- **On-Surface-Variant (`#6E5D53` — Café Grisáceo):** Textos secundarios, fechas de artículos, migas de pan y textos de ayuda.
- **Outline (`#E5D9CE` — Borde Cálido):** Bordes sutiles de inputs, tarjetas y divisores de sección.
- **Success (`#1E6B24` — Verde Botánico):** Mensajes de confirmación de reserva agendada o producto añadido al carrito.
- **Error (`#BA1A1A` — Rojo Terracota):** Mensajes de validación de campos obligatorios o problemas de stock.

## Typography

- **Títulos:** `Outfit` (sans-serif geométrica, moderna y con presencia editorial).
  - `headline-display` (48px, bold, interlineado 1.1): Título del Hero en desktop.
  - `headline-lg` (32px, semibold, interlineado 1.2): Encabezados de secciones principales (h2).
  - `headline-md` (24px, semibold, interlineado 1.25): Títulos de subsecciones y modales (h3).
  - `title-md` (18px, semibold, interlineado 1.3): Títulos de tarjetas de producto y nombres de artículos.
- **Textos:** `Plus Jakarta Sans` (sans-serif contemporánea, clara y óptima para móviles).
  - `body-md` (16px, regular, interlineado 1.6): Cuerpo general de párrafos y descripciones.
  - `body-sm` (14px, regular, interlineado 1.5): Textos secundarios, descripciones en tarjetas y notas al pie.
  - `label-md` (15px, semibold, interlineado 1.0): Textos de botones, inputs y navegación.
  - `label-sm` (13px, semibold, interlineado 1.0): Chips de categorías, badges de oferta y metadatos.

## Layout

- **Ancho máximo de contenedor:** 1200px centrado horizontalmente (`max-width: 1200px; margin: 0 auto;`).
- **Márgenes laterales:** 
  - Desktop: 32px
  - Tablet: 24px
  - Mobile: 16px
- **Escala de espaciado:** 4px (`xs`), 8px (`sm`), 16px (`md`), 24px (`lg`), 32px (`xl`), 48px (`2xl`), 64px (`3xl`).
- **Breakpoints y comportamiento responsive:**
  - **Mobile (hasta 767px):**
    - Contenedores al 100% de ancho con `padding: 0 16px`.
    - La navegación colapsa en un menú hamburguesa lateral accesible.
    - La tienda muestra **1 producto por fila** (o 2 en cuadrícula compacta de 375px si la pantalla lo amerita).
    - Los filtros de tienda se abren mediante un botón "Filtrar y Ordenar" en modal / drawer inferior.
    - El Hero organiza sus elementos verticalmente (texto arriba, imagen abajo, botones a ancho completo).
    - Los chips de categorías permiten scroll horizontal táctil sin saltos de línea.
  - **Tablet (768px a 1023px):**
    - La tienda muestra **2 productos por fila**.
    - El blog muestra **2 columnas de artículos**.
    - Barra de navegación visible con enlaces compactos.
  - **Desktop (1024px o más):**
    - La tienda muestra **3 productos por fila** junto a una barra lateral fija (`aside`) de filtros a la izquierda.
    - El blog muestra **3 columnas de artículos**.
    - La ficha de producto muestra un diseño de 2 columnas (galería de fotos a la izquierda, detalles y selector de compra a la derecha).
    - El carrito muestra los ítems a la izquierda (65% de ancho) y el resumen con cálculo de despacho a la derecha (35% de ancho).

## Elevation & Depth

- **Nivel 0 (Plano):** Fondos de página y tarjetas secundarias integradas (`box-shadow: none; border: 1px solid #E5D9CE`).
- **Nivel 1 (Superficie / Cards):** Tarjetas de blog y cajas de contenido (`box-shadow: 0 4px 16px rgba(123, 52, 30, 0.06)`).
- **Nivel 2 (Hover interactivo):** Tarjetas de producto en hover (`box-shadow: 0 10px 24px rgba(123, 52, 30, 0.12); transform: translateY(-4px); transition: all 0.25s ease`).
- **Nivel 3 (Modales y Navbar Sticky):** Navbar superior fija al hacer scroll y ventanas emergentes (`box-shadow: 0 12px 32px rgba(43, 29, 22, 0.16)`).

## Shapes

- **Botones y Badges (`rounded.full` — 9999px):** Forma redondeada completa estilo píldora para dar sensación orgánica, suave y accesible al tacto móvil.
- **Tarjetas de Producto y Blog (`rounded.lg` — 16px):** Esquinas curvadas pronunciadas para un look moderno y amigable.
- **Campos de Formulario e Inputs (`rounded.md` — 8px):** Radio equilibrado con borde definido para indicar interactividad.
- **Imágenes de Galería y Banners (`rounded.lg` — 16px):** Coherencia con el radio de las tarjetas contenedor.

## Components

### Botón Primario (`button-primary`)
- **Contenido:** Texto centrado en `label-md`, ícono opcional a la derecha (flecha o calendario).
- **Reglas:** Fondo `#7B341E`, texto `#FFFFFF`, radio píldora (`9999px`), padding `14px 28px`.
- **Estados:**
  - *Hover (`button-primary-hover`):* Fondo `#5E2713`, elevación sutil.
  - *Active:* Fondo `#4A1E0E`, transformación de escala `scale(0.98)`.
  - *Disabled (`button-primary-disabled`):* Fondo `#E2DDD8`, texto `#8C837C`, cursor no permitido.

### Botón Secundario (`button-secondary`)
- **Contenido:** Texto centrado en `label-md`, ícono opcional.
- **Reglas:** Fondo `#F5EBE1`, texto `#7B341E`, radio píldora (`9999px`), padding `14px 28px`.
- **Estados:**
  - *Hover (`button-secondary-hover`):* Fondo `#E5D9CE`, texto `#5E2713`.

### Tarjeta de Producto (`card-product`)
- **Contenido:** Imagen superior rectangular (proporción 4:3) con esquinas redondeadas de 12px, badge superior opcional (`tag-offer`), nombre del producto en `title-md` (máximo 2 líneas, truncate con `...`), calificación con 5 estrellas en color `#C87D20`, precio en CLP visible y destacado en `headline-md`, y botón secundario "Ver Detalle / Agregar".
- **Reglas:** Fondo `#F5EBE1`, borde `1px solid #E5D9CE`, radio `16px`, padding `16px`. El precio siempre es visible y no puede ocultarse tras una interacción.
- **Estados:**
  - *Hover:* Sombra Nivel 2 y la imagen aumenta ligeramente su escala (`scale(1.03)`).
  - *Agotado:* Imagen con filtro en escala de grises al 60%, badge "Agotado" en gris y botón deshabilitado.

### Tarjeta de Artículo de Blog (`card-article`)
- **Contenido:** Imagen de cabecera con ratio 16:9, chip de categoría (`tag-category`), título del artículo en `title-md`, metadatos (tiempo de lectura y fecha en `body-sm`), extracto de 2 líneas y enlace con flecha "Leer artículo".
- **Reglas:** Fondo `#FFFFFF`, radio `16px`, padding `24px`, elevación Nivel 1.
- **Estados:**
  - *Hover:* El título cambia de color a `#7B341E` y la tarjeta sube 3px.

### Formulario de Captación de Leads (`form-leads`)
- **Contenido:** Título en `headline-md`, descripción del beneficio, campo `input-field` para correo, botón `button-primary` con texto "Quiero mi Guía y Cupón" y microtexto de privacidad (`body-sm`).
- **Reglas:** Contenedor con fondo `#F5EBE1`, radio `16px`, padding `32px`, centrado.

### Selector / Cotizador de Servicios (`service-calculator`)
- **Contenido:** Pestañas de técnica (Knotless Braids, Box Braids, Cornrows), selector de largo mediante botones interactivos (Hombros / Espalda / Cintura), selector de grosor (Delgadas / Medianas / Gruesas), caja resumen con precio estimado calculado y botón "Agendar por WhatsApp".
- **Reglas:** La opción seleccionada toma el estilo `tag-category-active` (fondo `#7B341E`, texto `#FFFFFF`).

## Do's and Don'ts

### Do's (Lo que siempre se hace)
- **Siempre** mostrar los precios con formato claro en pesos chilenos (`$24.990 CLP`) en todas las tarjetas de producto y servicios.
- **Siempre** mantener el contraste accesible WCAG AA (mínimo 4.5:1) en todos los textos y botones.
- **Siempre** incluir badges informativos sobre las técnicas ("100% Sin dolor ni tracción agresiva") para brindar seguridad al cliente.
- **Siempre** diseñar y verificar el flujo completo en formato Mobile (375px de ancho) antes de pasar a escritorio.
- **Siempre** usar botones estilo píldora (`rounded.full`) para todas las llamadas a la acción (CTAs).

### Don'ts (Lo que nunca se hace)
- **Nunca** ocultar el precio de un servicio o producto para obligar al usuario a enviar un mensaje privado por Instagram.
- **Nunca** usar texto blanco sobre el color de acento `#C87D20` sin utilizar la variante accesible `#8E4506`.
- **Nunca** aplicar más de dos tipografías distintas en una misma página.
- **Nunca** utilizar imágenes genéricas pixeladas o que no representen fielmente el trabajo de trenzado profesional.
- **Nunca** permitir que un contenedor sobrepase los `1200px` de ancho máximo en pantallas ultra-anchas.
