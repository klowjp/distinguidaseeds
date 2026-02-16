---
name: modo-produccion
description: Revisa una app/landing, detecta problemas típicos, propone mejoras y aplica correcciones con un checklist fijo para dejarlo listo para enseñar o publicar.
---

# Modo Producción (QA + Fix)

## Cuándo usar este skill

- Cuando ya tienes algo generado (landing/app) y quieres dejarlo "presentable".
- Cuando algo funciona "a medias" (móvil raro, imágenes rotas, botones sin acción, espaciados feos).
- Antes de enseñarlo a un cliente, grabarlo o publicarlo.

## Inputs necesarios

> Si falta alguno, **pregunta primero** antes de revisar.

1. **Archivo principal** - por ejemplo `index.html` o ruta del proyecto
2. **Objetivo de la revisión** - "lista para enseñar" o "lista para publicar"
3. **Restricciones** - no cambiar branding / no cambiar copy / no tocar estructura, etc.

## Checklist de calidad (orden fijo)

### A) Funciona y se ve
- [ ] Abre la preview / localhost sin errores
- [ ] Imágenes cargan y no hay rutas rotas
- [ ] Tipografías y estilos se aplican correctamente

### B) Responsive (móvil primero)
- [ ] Se ve bien en móvil (no se corta, no hay scroll horizontal)
- [ ] Botones y textos tienen tamaños legibles
- [ ] Secciones con espaciado coherente

### C) Copy y UX básica
- [ ] Titular claro y coherente con la propuesta
- [ ] CTAs consistentes (mismo verbo, misma intención)
- [ ] No hay texto "placeholder" tipo lorem ipsum

### D) Accesibilidad mínima
- [ ] Contraste razonable en textos
- [ ] Imágenes con alt
- [ ] Estructura de headings (h1, h2) lógica

## Workflow

### Paso 1: Diagnóstico rápido
- Revisa el proyecto siguiendo el checklist A→B→C→D
- Lista 5–10 problemas encontrados (priorizados de mayor a menor impacto)

### Paso 2: Plan de arreglos
- Propón máximo 8 cambios
- Formato: "qué cambio y por qué"

### Paso 3: Aplicar cambios
- Modifica los archivos necesarios
- Un cambio a la vez, verificando que no rompe nada

### Paso 4: Validación
- Vuelve a abrir preview
- Confirma que el checklist pasa

### Paso 5: Resumen final
- Lista de cambios hechos
- Qué queda opcional para mejorar (si aplica)

## Reglas

- **Respeta el skill de marca:** si existe `estilo-marca`, no cambies colores ni tipografías.
- **No rehagas todo:** corrige lo mínimo para ganar calidad rápido.
- **Claridad > bonito:** si hay conflicto, prioriza que se entienda.
- **Móvil primero:** siempre revisa en viewport pequeño antes que desktop.

## Output (formato exacto)

Devuelve siempre en este orden:

---

### 1) Diagnóstico

**Problemas encontrados (priorizados):**

| # | Problema | Categoría | Impacto |
|---|----------|-----------|---------|
| 1 | [Descripción] | A/B/C/D | Alto/Medio/Bajo |
| 2 | [Descripción] | A/B/C/D | Alto/Medio/Bajo |
| ... | ... | ... | ... |

---

### 2) Cambios aplicados

| # | Archivo | Cambio | Por qué |
|---|---------|--------|---------|
| 1 | [archivo.ext] | [Qué se modificó] | [Razón] |
| 2 | [archivo.ext] | [Qué se modificó] | [Razón] |
| ... | ... | ... | ... |

---

### 3) Resultado

**Estado:** ✅ OK para enseñar / ✅ OK para publicar / ⚠️ Pendiente

**Checklist final:**
- [x] A) Funciona y se ve
- [x] B) Responsive
- [x] C) Copy y UX
- [x] D) Accesibilidad

**Notas:** [Observaciones o mejoras opcionales para el futuro]

---

## Manejo de errores

- Si hay demasiados problemas → prioriza los 8 más críticos, el resto va a "mejoras opcionales".
- Si no puedo abrir la preview → pido al usuario que confirme que funciona.
- Si las restricciones bloquean un fix importante → aviso y sugiero alternativa.
