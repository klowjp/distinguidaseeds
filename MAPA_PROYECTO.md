# 🗺️ Mapa del Proyecto: DISTINGUIDA SEEDS

Este documento sirve como la única fuente de verdad para la estructura y nomenclatura de las secciones del sitio web. **PROHIBIDO** cambiar nombres de IDs o clases estructurales sin actualizar este mapa.

## 🏗️ Estructura Global
- **Archivo Principal**: `index.html`
- **Tecnologías**: HTML5, Tailwind CSS, Iconify, JavaScript (Vanilla).
- **Estética**: Brutalismo Premium / Glassmorphism / Dark Mode (Neutral-950).

---

## 📍 Secciones del Sitio

### 1. 🧭 Navigation (`#main-nav-container`)
- **Tipo**: Barra de navegación flotante tipo "Pill".
- **Comportamiento**: Aparece después de 100px de scroll.
- **Elementos**: Logo, Enlaces (Genética, Semillas, Nosotros, Garantía, Envíos), Buscador y Menú.

### 2. ⚡ Hero Section (`<header>`)
- **Identificador**: Sin ID (etiqueta `header`).
- **Elementos Clave**:
  - **Background**: Imagen cinemática con overlay gradiente.
  - **Merged Data Card (Top Right)**: Tarjeta de "Bogotá: Genética Activa" con manifiesto y stats (Maestría y Cepas F1 en verde).
  - **Headline**: "GENÉTICA & MAESTRÍA".
  - **Status Card (Bottom Left)**: Tarjeta simétrica pequeña con "Porcentaje de éxito" (99.9%) y barra de progreso.
  - **Scroll Indicator**: Animación de mouse al centro inferior.

### 3. 🧬 Collection / Projects (`#projects`)
- **Título**: "Nuestra Colección."
- **Nomenclatura**: Cepas F1.
- **Filtros**: "Todas las Cepas", "Más Potentes", "Sabor & Aroma".
- **Tarjetas Dynamic Grid**:
  - `card-distinguida`: (La más grande/Star).
  - `card-manjar`: (Stack derecho).
  - `card-toystone`: (Stack derecho).
  - `card-misterio`: (Stack derecho).

### 4. 📊 Genetic Analysis (`#analytics`)
- **Título**: "Perfiles Terpénicos."
- **Contenido**: 4 tarjetas horizontales con ecualizadores dinámicos (`.bar-anim`).
- **Comportamiento**: Animación de 1.5s al hacer scroll y bucle infinito en hover.

### 5. 🛡️ Infrastructure / Promise (`#infrastructure`)
- **Título**: "Maestría Inquebrantable / Genética F1".
- **Elementos**: Puntos clave (Estándar de Oro, Éxito Asegurado) y Mapa Interactivo con Hotspots (Laboratorio y Control de Calidad).

### 6. 📜 About / History (`#about`)
- **Título**: "El Ascenso de la Distinguida".
- **Estructura**: Línea de tiempo (1994, 2012, 2024) con animaciones de slide lateral.

### 7. 🔒 Guarantee & Success (`#guarantee`)
- **Título**: "Tu Éxito es Nuestra Prioridad".
- **Contenido**: Seguimiento Visual y Asesoría IA.

### 8. 🚚 Shipping & Logistics (`#shipping`)
- **Título**: "Envíos Seguros & Discretos".
- **Elementos**: Lista de beneficios (Discreción, Crypto Pagos, Garantía) y Sede Central (Bogotá).

### 9. 🏛️ Footer (`<footer>`)
- **Contenido**: Información de marca, Enlaces rápidos, Métodos de pago (Crypto) y créditos legales.

---

## 🎨 Paleta de Colores
- **Fondo**: `bg-neutral-950`
- **Acento**: `text-emerald-500` / `bg-emerald-500`
- **Texto Principal**: `text-white` / `text-white/90`
- **Texto Secundario**: `text-white/40`
- **Bordes/Líneas**: `border-white/10` / `bg-white/5`

## ⚙️ Reglas de Oro para Ediciones
1. **NO** modificar colores de valores estadísticos (30+ Años, etc.) si ya son blancos.
2. **NO** cambiar etiquetas de "Porcentaje de éxito" a versiones cortas.
3. **NO** añadir textos como "Sistema Operativo" o "Est. 1994" si fueron eliminados.
4. **Respetar** el vocabulario: "Moderado/Moderada" en lugar de "Baja/Bajo".
5. **Cuidar Simetría**: La tarjeta de éxito inferior izquierda debe ser siempre compacta (`w-48`).
