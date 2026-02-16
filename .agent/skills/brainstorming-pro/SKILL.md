---
name: brainstorming-pro
description: Genera ideas de calidad con estructura, filtros y selección final. Úsalo cuando necesites opciones creativas con criterio y una recomendación clara.
---

# Brainstorming Pro

## Cuándo usar este skill

- Cuando el usuario pida ideas, variantes, conceptos, hooks, nombres, formatos o enfoques.
- Cuando haya bloqueo creativo o demasiadas opciones y haga falta ordenar.
- Cuando el usuario necesite ideas "buenas para ejecutar", no solo ocurrencias.

## Inputs necesarios

> Si falta alguno, **pregunta primero** antes de generar.

1. **Objetivo exacto** - qué se quiere conseguir
2. **Público / contexto** - para quién es y dónde se usa
3. **Restricciones** - tiempo, presupuesto, tono, formato, herramientas
4. **Ejemplos de lo que SÍ y lo que NO** - si el usuario tiene preferencias

## Workflow

### Paso 1: Aclarar el encargo
- Si faltan datos, haz 3–5 preguntas rápidas primero.
- No asumas. Pregunta.

### Paso 2: Generar ideas en 4 tandas

| Bloque | Cantidad | Criterio |
|--------|----------|----------|
| **A) Ideas rápidas** | 10 | Claras y ejecutables |
| **B) Ideas diferentes** | 5 | Ángulos no obvios |
| **C) Ideas low effort** | 5 | Rápidas de producir |
| **D) Ideas high impact** | 3 | Más ambiciosas y potentes |

### Paso 3: Filtrar y puntuar
Evalúa cada idea del 1 al 5 en:
- **Impacto** - cuánto mueve la aguja
- **Claridad** - se entiende a la primera
- **Novedad** - no es lo típico
- **Esfuerzo** - cuánto cuesta hacerlo
- **Viabilidad** - se puede ejecutar con los recursos disponibles

### Paso 4: Seleccionar TOP 5
Para cada idea del TOP 5, incluir:
- **Idea** (1 línea)
- **Por qué funciona** (2 líneas)
- **Primer paso** (1 línea)

## Reglas de calidad

- **Nada genérico.** Prohibido "mejorar tu productividad". Concreta siempre.
- **Hooks/títulos:** cortos y con tensión o curiosidad.
- **Formatos:** incluir estructura + ejemplo de primer minuto.
- **Incertidumbre:** si una idea depende de algo incierto, dilo y ofrece alternativa.

## Output (formato exacto)

Devuelve siempre en este orden:

---

### 1) Preguntas rápidas
*(Solo si faltan datos. Si están completos, salta a Ideas.)*

1. [Pregunta 1]
2. [Pregunta 2]
3. ...

---

### 2) Ideas

**Bloque A: Ideas rápidas (10)**
1. [Idea clara y ejecutable]
2. ...

**Bloque B: Ideas diferentes (5)**
1. [Ángulo no obvio]
2. ...

**Bloque C: Ideas low effort (5)**
1. [Rápida de producir]
2. ...

**Bloque D: Ideas high impact (3)**
1. [Ambiciosa y potente]
2. ...

---

### 3) TOP 5 recomendado

| # | Idea | Impacto | Claridad | Novedad | Esfuerzo | Viabilidad | Total |
|---|------|---------|----------|---------|----------|------------|-------|
| 1 | ... | 5 | 5 | 4 | 3 | 4 | 21 |
| 2 | ... | ... | ... | ... | ... | ... | ... |

**Detalle TOP 5:**

**1. [Idea]**
- Por qué funciona: [2 líneas]
- Primer paso: [1 línea]

**2. [Idea]**
- Por qué funciona: [2 líneas]
- Primer paso: [1 línea]

*(continúa hasta el 5)*

---

## Manejo de errores

- Si el output no cumple el formato → vuelve al paso 2, ajusta y regenera.
- Si hay ambigüedad en el objetivo → pregunta antes de asumir.
- Si el usuario no está satisfecho → pide feedback específico y genera nueva tanda.
