# Spec de diseño — Andjelica Braids Studio

> Guía: [Spec de diseño](../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)

La spec de diseño tiene dos partes:

1. **[`DESIGN.md`](../DESIGN.md)** (en la raíz): el design system con tokens, variables y reglas visuales que Google Stitch importa directamente.
2. **Este documento:** las 6 pantallas principales del proyecto estructuradas como prompts listos para generar en Stitch con contenido y componentes reales.

**Wireframes en Whimsical:** [Ver wireframes completos en Whimsical](https://whimsical.com/andjelica-braids-studio-wireframes-W7qZ3v9)

> Guía de wireframes: [Wireframes](../evaluacion/guias/fase-2-specs/04-wireframes.md)

![Wireframes de Andjelica Braids Studio](img/wireframes.png)

---

## Pantallas

### 1. Landing Page (Inicio)

```text
Pantalla: Landing Page de Andjelica Braids Studio, versión desktop (1200px de ancho máximo centrado, fondo #FDFBF7). Usa el design system del proyecto (DESIGN.md).
Objetivo: Valeria debe entender en 5 segundos los servicios de trenzado profesional sin dolor, cotizar un estilo de trenzas, ver insumos destacados y captar su correo a cambio de una guía de cuidados con 10% de descuento.

Componentes, de arriba hacia abajo:
1. Navbar Global: Logo "Andjelica Braids Studio", enlaces de navegación (Inicio, Servicios y Tienda, Blog, Sobre Mí, Contacto), buscador con input-field "Buscar estilos o productos...", botón button-primary "Agendar Cita" e ícono de carrito de compras con badge de 2 productos.
2. Hero Section:
   - Columna izquierda: Tag tag-offer con texto "✨ Trenzado Profesional en Valparaíso", título principal en headline-display "Resalta tu belleza con trenzas impecables y sin dolor", bajada en body-md "Especialistas en knotless box braids, cornrows y peinados protectores con asesoría personalizada y cuidado experto de tu cabello natural", fila de botones con button-primary "Cotizar y Agendar Peinado" y button-secondary "Ver Tienda e Insumos", y badge de confianza con ícono de corazón "Más de 400 clientas felices · Técnica sin tensión agresiva".
   - Columna derecha: Fotografía editorial en alta resolución de clienta luciendo Knotless Braids con acabado brillante, dentro de contenedor con bordes redondeados rounded.lg y sombra suave.
3. Sección de Beneficios Clave (3 columnas con fondo #F5EBE1 y radio rounded.lg):
   - Tarjeta 1: Ícono de pluma + Título "Cero Tensión y Sin Dolor" + Texto "Cuidamos la raíz y el cuero cabelludo para que disfrutes tu peinado desde el primer día".
   - Tarjeta 2: Ícono de diamante + Título "Insumos Premium" + Texto "Kanekalon ultraligero y productos hidratantes libres de escamas blancas o alcohol".
   - Tarjeta 3: Ícono de reloj + Título "Precios y Tiempos Transparentes" + Texto "Conoce exactamente cuánto cuesta y cuántas horas toma tu sesión antes de agendar".
4. Cotizador y Selector Interactivo de Servicios (service-calculator):
   - Encabezado: h2 headline-lg "Simula tu Peinado Ideal" y bajada "Elige el estilo, largo y grosor para conocer el valor estimado".
   - Controles interactivos: Chips tag-category para técnica (Knotless Box Braids [activo], Cornrows / Pegadas, Goddess Braids), selector de largo (Hombros $35.000, Espalda $45.000, Cintura $55.000), selector de grosor (Delgadas, Medianas, Gruesas).
   - Caja de resultado en fondo #FFFFFF con radio rounded.md: "Total estimado: $45.000 CLP · Tiempo estimado: 4.5 horas" y botón button-primary "Reservar este Estilo por WhatsApp".
5. Sección Destacados de Tienda (Fila de 3 card-product):
   - Card 1: Foto "Kanekalon Jumbo Tono 1B Negro Natural" + tag-offer "Más vendido" + Precio "$4.990 CLP" + button-secondary "Ver Producto".
   - Card 2: Foto "Mousse Fijador Anti-Frizz con Argán 250ml" + tag-offer "Esencial" + Precio "$8.990 CLP" + button-secondary "Ver Producto".
   - Card 3: Foto "Gorro de Satén Doble Capa Ajustable" + tag-offer "Protección" + Precio "$6.990 CLP" + button-secondary "Ver Producto".
6. Sección de Testimonios y Galería de Trabajos Reales:
   - Título en headline-lg "La experiencia de nuestras clientas", grilla de 3 tarjetas de reseña con 5 estrellas en #C87D20, foto real del peinado, comentario y nombre de la clienta ("Valeria M. — ¡Por fin una trenzadora que no me tironea el pelo! Me duraron 6 semanas perfectas").
7. Formulario de Captación de Leads (form-leads):
   - Contenedor con fondo #F5EBE1 y padding de 32px: Título en headline-md "Descarga gratis nuestra Guía de Cuidado de Trenzas en PDF", bajada "Aprende cómo lavar, dormir y mantener tus trenzas perfectas + obtén 10% OFF en tu primera cita o compra", campo input-field "Ingresa tu correo electrónico", botón button-primary "Obtener Guía y Descuento" y microtexto "Tus datos están protegidos. Sin spam.".
8. Footer Global: 4 columnas con logo y descripción, enlaces a políticas y páginas obligatorias (Preguntas Frecuentes, Términos y Condiciones, Política de Privacidad, 404), horario de atención en Valparaíso y enlaces a redes sociales (@andjelicabraids en Instagram y TikTok).
```

---

### 2. Tienda y Catálogo de Insumos

```text
Pantalla: Tienda y Catálogo de Andjelica Braids Studio, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Valeria busca y filtra productos e insumos capilares (kanekalon, mousses, geles y accesorios) por categoría y rango de precio, visualizando precios claros en CLP y disponibilidad inmediata.

Componentes, de arriba hacia abajo:
1. Navbar Global (con badge de carrito actualizado).
2. Encabezado de Página:
   - Título en headline-lg "Tienda de Insumos y Cuidados Capilares".
   - Bajada en body-md "Productos probados y recomendados en nuestro estudio para preparar, peinar y mantener tus trenzas impecables".
   - Buscador amplio input-field con texto placeholder "Buscar kanekalon, gel de bordes, mousse, gorros...".
3. Barra de Categorías Rápidas (Fila de chips horizontales):
   - Chips: "Todos los productos" (tag-category), "Extensiones de Kanekalon" (tag-category-active), "Cuidado y Fijación" (tag-category), "Accesorios y Satén" (tag-category).
4. Layout Principal de Tienda (2 columnas: Aside de filtros a la izquierda de 280px + Grilla de productos a la derecha de 880px):
   - Barra lateral de Filtros (Aside con fondo #FFFFFF, padding 20px, radio rounded.md y borde outline):
     - Bloque 1: Filtro por Tipo de Uso (Checkboxes: Para el momento del trenzado, Mantenimiento diario, Retiro de trenzas).
     - Bloque 2: Rango de Precio (Slider interactivo de $3.000 a $25.000 CLP).
     - Bloque 3: Disponibilidad (Checkbox: Solo con stock inmediato en Valparaíso).
     - Botón button-secondary "Limpiar Filtros".
   - Grilla de Productos (3 columnas con 6 card-product):
     - Producto 1: Foto "Kanekalon Ombré Tono T1B/30 Castaño Miel" + tag-offer "Tendencia" + Estrellas 5.0 + Precio "$5.990 CLP" + button-secondary "Ver Detalle".
     - Producto 2: Foto "Gel Fijador Edge Control Extra Fuerte 100g" + tag-offer "Sin residuos" + Estrellas 4.9 + Precio "$7.490 CLP" + button-secondary "Ver Detalle".
     - Producto 3: Foto "Mousse Espumoso Anti-Frizz con Aceite de Argán" + tag-offer "Recomendado" + Estrellas 5.0 + Precio "$8.990 CLP" + button-secondary "Ver Detalle".
     - Producto 4: Foto "Gorro de Satén Doble Faz Rosa/Champagne" + Estrellas 4.8 + Precio "$6.990 CLP" + button-secondary "Ver Detalle".
     - Producto 5: Foto "Aceite Nutritivo de Romero y Menta para Cuero Cabelludo 60ml" + tag-offer "Alivio picazón" + Estrellas 5.0 + Precio "$9.990 CLP" + button-secondary "Ver Detalle".
     - Producto 6: Foto "Pack 20 Anillos Metálicos Decorativos Dorados" + Estrellas 4.7 + Precio "$3.490 CLP" + button-secondary "Ver Detalle".
5. Paginación / Cargar más: Botón button-secondary centrado "Cargar más productos".
6. Banner Informativo de Despacho: Fondo #F5EBE1 con texto "🚚 Envíos a todo Chile vía Starken/Chilexpress y retiro gratis en nuestro estudio de Valparaíso".
7. Footer Global.
```

---

### 3. Ficha de Detalle de Producto

```text
Pantalla: Ficha de Detalle de Producto de Andjelica Braids Studio, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Valeria examina a fondo un insumo específico ("Mousse Fijador Anti-Frizz con Aceite de Argán"), selecciona la variante/tamaño, conoce cómo usarlo en sus trenzas y lo agrega al carrito o consulta por WhatsApp.

Componentes, de arriba hacia abajo:
1. Navbar Global.
2. Migas de Pan (Breadcrumbs): Texto en text-secondary "Inicio / Tienda / Cuidado y Fijación / Mousse Fijador Anti-Frizz".
3. Layout de Detalle de Producto (2 columnas de 50% cada una):
   - Columna Izquierda (Galería de Imágenes): Imagen principal de alta calidad (botella de mousse espumoso aplicada sobre trenzas limpias) con radio rounded.lg + miniatura de 3 fotos secundarias (aplicación en textura, envase, clienta con peinado terminado).
   - Columna Derecha (Información de Compra y Selección):
     - Badge tag-offer "Esencial para Mantenimiento".
     - Título del producto en headline-lg "Mousse Fijador Anti-Frizz con Aceite de Argán".
     - Calificación con estrellas (5.0 / 38 reseñas verificadas).
     - Precio destacado en headline-display "$8.990 CLP".
     - Selector de Presentación/Variante: Botones chips "250 ml ($8.990 CLP) [activo]" y "500 ml Familiar ($14.990 CLP)".
     - Selector de Cantidad (Controles - 1 +) y botón button-primary "Agregar al Carrito".
     - Botón secundario de WhatsApp con ícono: "Consultar a la trenzadora por WhatsApp".
     - Cuadro de beneficios rápidos: "✔️ No deja escamas blancas", "✔️ Fórmula sin alcohol secante", "✔️ Despacho en 24-48 hrs".
4. Pestañas de Información Técnica y Guía de Uso (Tabs sobre fondo #FFFFFF, radio rounded.md, padding 24px):
   - Tab 1 (Modo de Uso): Pasos ilustrados: "1. Aplica 2 o 3 pulsaciones sobre las trenzas húmedas o secas. 2. Distribuye suavemente con las palmas de arriba hacia abajo. 3. Coloca tu gorro de satén por 10 minutos para fijar sin frizz."
   - Tab 2 (Ingredientes): "Aceite de argán marroquí puro, agua desmineralizada, glicerina vegetal, extracto de aloe vera. Libre de parabenos y sulfatos."
   - Tab 3 (Preguntas de clientas): "¿Sirve para trenzas con kanekalon? Sí, sella la fibra sintética y mantiene el brillo del peinado."
5. Sección de Productos Complementarios (Fila de 3 card-product con kanekalon, gorro de satén y aceite de romero).
6. Footer Global.
```

---

### 4. Carrito de Compras

```text
Pantalla: Carrito de Compras de Andjelica Braids Studio, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Valeria revisa los productos agregados, calcula el costo de despacho a su comuna antes de pagar, aplica su cupón de 10% y avanza al checkout con total transparencia sin costos ocultos.

Componentes, de arriba hacia abajo:
1. Navbar Global.
2. Encabezado de Carrito: h1 en headline-lg "Tu Carrito de Compras (2 productos)".
3. Layout Principal del Carrito (2 columnas: Lista de productos 65% a la izquierda + Resumen y despacho 35% a la derecha):
   - Columna Izquierda (Tabla / Lista de Ítems en tarjetas con fondo #FFFFFF y radio rounded.md):
     - Ítem 1: Miniatura de foto + Título "Mousse Fijador Anti-Frizz (250ml)" + Precio unitario "$8.990 CLP" + Selector de cantidad [1] + Subtotal "$8.990 CLP" + Botón eliminar (ícono papelera).
     - Ítem 2: Miniatura de foto + Título "Gorro de Satén Doble Capa (Rosa/Champagne)" + Precio unitario "$6.990 CLP" + Selector de cantidad [1] + Subtotal "$6.990 CLP" + Botón eliminar.
     - Enlace inferior: "← Seguir comprando en la tienda".
   - Columna Derecha (Resumen del Pedido con fondo #F5EBE1, radio rounded.lg, padding 24px):
     - Título en headline-md "Resumen del Pedido".
     - Subtotal: "$15.980 CLP".
     - Simulador de Costo de Despacho (Propia):
       - Selector desplegable de Región: "Región de Valparaíso [seleccionada]".
       - Selector desplegable de Comuna: "Valparaíso / Viña del Mar [seleccionada]".
       - Tarifa calculada: "$2.990 CLP (Entrega estimada: 24 a 48 hrs)" con opción alternativa "Retiro gratuito en estudio (Cerro Alegre)".
     - Campo de Cupón de Descuento: input-field "Ingresa cupón (ej: VALERIA10)" + botón secundario "Aplicar" → Aplica -$1.598 CLP con mensaje message-success "¡Cupón de 10% aplicado!".
     - Divisor y Total Final Destacado en headline-md: "$17.372 CLP".
     - Botón principal de acción button-primary a ancho completo: "Proceder al Pago Seguro".
     - Badges de seguridad: Íconos de Webpay / Transferencia bancaria segura + "Garantía de satisfacción y soporte vía WhatsApp".
4. Footer Global.
```

---

### 5. Blog y Consejos de Cuidado

```text
Pantalla: Blog de Andjelica Braids Studio, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Valeria navega y filtra artículos educativos sobre mantenimiento de trenzas, estilos en tendencia y salud capilar para aprender a cuidar su cabello natural.

Componentes, de arriba hacia abajo:
1. Navbar Global.
2. Hero del Blog:
   - Título en headline-display "El Blog del Trenzado y la Salud Capilar".
   - Bajada en body-md "Consejos profesionales, guías paso a paso y secretos de cuidado para que tus peinados protectores duren más tiempo impecables y saludables".
3. Barra de Categorías del Blog (Chips interactivos tag-category):
   - "Todos los artículos" (tag-category), "Cuidados y Mantenimiento" (tag-category-active), "Estilos y Tendencias" (tag-category), "Salud Capilar y Transición" (tag-category).
4. Artículo Destacado Principal (Banner horizontal de 2 columnas con fondo #F5EBE1 y radio rounded.lg):
   - Izquierda: Imagen amplia de lavado suave de trenzas.
   - Derecha: Tag tag-offer "Guía más leída" + Título en headline-lg "Cómo lavar y secar tus trenzas paso a paso sin arruinar el peinado" + Extracto en body-md "Descubre la técnica de lavado con difusor y espuma que evita el frizz, elimina la picazón y protege tu cabello natural sin desarmar las trenzas." + Metadatos "5 min de lectura · Por Andjelica" + Botón button-primary "Leer Guía Completa".
5. Grilla de Artículos Recientes (3 columnas con 6 card-article):
   - Card 1: Foto + Tag "Estilos y Tendencias" + Título "Knotless vs. Box Braids tradicionales: ¿cuál es la mejor opción para tu cuero cabelludo?" + 4 min de lectura + Enlace "Leer artículo →".
   - Card 2: Foto + Tag "Salud Capilar" + Título "Cómo preparar tu cabello natural antes de tu cita de trenzado" + 3 min de lectura + Enlace "Leer artículo →".
   - Card 3: Foto + Tag "Cuidados y Mantenimiento" + Título "Por qué el gorro de satén es el mejor amigo de tus trenzas al dormir" + 3 min de lectura + Enlace "Leer artículo →".
   - Card 4: Foto + Tag "Salud Capilar" + Título "5 señales de que es hora de retirar tus trenzas para proteger tu raíz" + 4 min de lectura + Enlace "Leer artículo →".
   - Card 5: Foto + Tag "Estilos y Tendencias" + Título "French Curls y Goddess Braids: la tendencia de rizos que domina esta temporada" + 5 min de lectura + Enlace "Leer artículo →".
   - Card 6: Foto + Tag "Cuidados y Mantenimiento" + Título "Rutina nocturna en 3 pasos para mantener los bordes (baby hairs) perfectos" + 3 min de lectura + Enlace "Leer artículo →".
6. Caja de Suscripción al Blog (form-leads): Título "¿Quieres recibir nuevos tips de trenzado y ofertas exclusivas?" + input de email + botón "Suscribirme".
7. Footer Global.
```

---

### 6. Artículo de Blog Detallado

```text
Pantalla: Artículo de Blog Individual de Andjelica Braids Studio, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Valeria lee la guía paso a paso sobre lavado y secado, encuentra productos recomendados para su rutina capilar, interactúa comentando sus dudas y comparte el artículo en redes sociales.

Componentes, de arriba hacia abajo:
1. Navbar Global.
2. Cabecera del Artículo:
   - Migas de pan: "Inicio / Blog / Cuidados y Mantenimiento / Cómo lavar y secar tus trenzas".
   - Chip tag-category "Cuidados y Mantenimiento".
   - Título en headline-display "Cómo lavar y secar tus trenzas paso a paso sin arruinar el peinado".
   - Metadatos: "Publicado por Andjelica · 5 min de lectura · 12 comentarios".
3. Imagen Principal del Artículo: Fotografía nítida en ratio 16:9 con esquinas redondeadas rounded.lg.
4. Cuerpo del Artículo (Contenedor de lectura de 780px centrado, tipografía body-md con interlineado 1.8):
   - Introducción sobre la importancia de mantener el cuero cabelludo limpio para evitar acumulación de sebo.
   - Encabezado h2 headline-lg "Paso 1: Diluye tu shampoo en una botella con aplicador".
   - Párrafo explicativo y consejo pro.
   - Encabezado h2 headline-lg "Paso 2: Masajea solo el cuero cabelludo, no frotes las trenzas".
   - Párrafo explicativo.
   - Cuadro Destacado de Producto Recomendado (card-product incrustada con fondo #F5EBE1):
     - Foto de "Mousse Fijador con Aceite de Argán" + Texto "Para sellar y devolver el brillo tras el lavado" + Precio "$8.990 CLP" + Botón button-primary "Comprar Insumo".
   - Encabezado h2 headline-lg "Paso 3: Secado total con secador en aire tibio o frío".
   - Párrafo de advertencia sobre no acostarse con trenzas húmedas.
5. Bloque para Compartir en Redes Sociales:
   - Texto "Comparte esta guía con tus amigas:" + Botones con íconos de WhatsApp, Instagram Stories, Pinterest y Copiar Enlace.
6. Sección de Comentarios de Lectoras:
   - Título en headline-md "Comentarios (2)".
   - Comentario 1: "Valeria M. — ¡Excelente tutorial! ¿El mousse se aplica con el pelo 100% seco o húmedo?" + Respuesta de la autora "Andjelica: ¡Hola Valeria! Lo ideal es aplicarlo con el cabello ligeramente húmedo y luego secarlo para que selle perfecto".
   - Formulario de Nuevo Comentario: Campo textarea input-field "Escribe tu pregunta o comentario...", campos de nombre y correo, y botón button-primary "Publicar Comentario".
7. Artículos Relacionados (Fila de 3 card-article).
8. Footer Global.
```

---

### Versión Mobile (Prompt para cada pantalla en 375px)

```text
Genera la versión mobile (375px de ancho) de esta pantalla siguiendo estrictamente la sección Layout de DESIGN.md:
- Todos los contenedores ocupan el 100% del ancho de pantalla con márgenes laterales de 16px.
- La barra de navegación superior colapsa en un header compacto con logotipo, ícono de lupa para búsqueda, ícono de carrito con badge y botón de menú hamburguesa accesible.
- En la tienda, los productos se disponen en 1 sola columna vertical con tarjetas card-product adaptadas (o cuadrícula compacta), y los filtros de búsqueda se activan mediante un botón flotante/fijo "Filtrar y Ordenar" que despliega un drawer modal inferior.
- En el hero y fichas de producto, las columnas se apilan verticalmente (texto e información arriba, imagen abajo, botones de acción a ancho completo de 100%).
- Los chips de categorías tag-category se ordenan en una barra de desplazamiento horizontal táctil (scroll-x suave) sin cortar el texto ni desbordar la pantalla.
- La tipografía escala según los tamaños mobile definidos en DESIGN.md (h1 a 2.25rem, h2 a 1.75rem, párrafos a 1rem) manteniendo botones táctiles amplios de mínimo 48px de altura de toque.
```
