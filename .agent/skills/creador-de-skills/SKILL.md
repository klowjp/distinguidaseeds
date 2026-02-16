---
name: creador-de-skills
description: Diseña Skills predecibles y reutilizables para Antigravity. Úsalo cada vez que el usuario pida crear un skill nuevo o convertir un proceso en procedimiento estándar.
---

# Skill: Creador de Skills

Eres un experto en diseñar Skills para el entorno de Antigravity. Tu objetivo es crear Skills predecibles, reutilizables y fáciles de mantener, con una estructura clara de carpetas y una lógica que funcione bien en producción.

## Cuándo usar este skill

- Cuando el usuario pida "créame un skill para X"
- Cuando el usuario repita un proceso y quiera estandarizarlo
- Cuando se necesite un estándar de formato reutilizable
- Cuando haya que convertir un prompt largo en un procedimiento estándar

## Inputs necesarios

1. **Nombre del skill** - corto, en minúsculas, con guiones (máx 40 caracteres)
2. **Propósito** - qué problema resuelve o qué tarea automatiza
3. **Triggers** - cuándo debe activarse
4. **Inputs del skill** - qué datos necesita para funcionar
5. **Output esperado** - formato exacto de la salida

> Si falta algún input crítico, **pregunta antes de generar**.

## Workflow

### Fase 1: Planificación
1) Entender el objetivo del skill
2) Identificar triggers claros
3) Definir inputs necesarios
4) Determinar formato de output exacto

### Fase 2: Diseño
5) Elegir nivel de libertad:
   - **Alta** (heurísticas): brainstorming, ideas, alternativas
   - **Media** (plantillas): documentos, copys, estructuras
   - **Baja** (pasos exactos): operaciones frágiles, scripts, cambios técnicos
6) Escribir workflow de 3-6 pasos (skills simples) o fases (skills complejos)
7) Definir checklist de validación

### Fase 3: Generación
8) Crear estructura de carpeta
9) Escribir SKILL.md con frontmatter YAML
10) Agregar recursos opcionales solo si aportan valor real

## Estructura mínima obligatoria

```
.agent/skills/<nombre-del-skill>/
├── SKILL.md           ← obligatorio (lógica y reglas)
├── recursos/          ← opcional (guías, plantillas, tokens)
├── scripts/           ← opcional (utilidades ejecutables)
└── ejemplos/          ← opcional (implementaciones de referencia)
```

**Regla:** No crees archivos innecesarios. Mantén la estructura lo más simple posible.

## Reglas de SKILL.md

### Frontmatter YAML (obligatorio)
```yaml
---
name: <nombre-del-skill>
description: <descripción breve en tercera persona, máx 220 caracteres>
---
```

### Reglas de nombre
- Corto, en minúsculas, con guiones
- Máximo 40 caracteres
- No uses nombres de herramientas salvo que sea imprescindible
- Ejemplos: `planificar-video`, `auditar-landing`, `responder-emails`

### Principios de escritura
- **Claridad sobre longitud:** pocas reglas, pero muy claras
- **No relleno:** evita explicaciones tipo blog, es un manual de ejecución
- **Separación:** estilo va a recursos, pasos van al workflow
- **Pedir datos:** si un input es crítico, el skill debe preguntar
- **Salida estandarizada:** define exactamente qué formato devuelves

## Checklist antes de entregar

- [ ] ¿Entendí el objetivo final?
- [ ] ¿Tengo todos los inputs necesarios?
- [ ] ¿Definí el output exacto?
- [ ] ¿Apliqué las restricciones correctas?
- [ ] ¿El nivel de libertad es el adecuado?
- [ ] ¿La estructura es la mínima necesaria?

## Manejo de errores

- Si el output no cumple el formato → vuelve al paso de diseño, ajusta restricciones y regenera
- Si hay ambigüedad → pregunta antes de asumir
- Si falta un input crítico → solicítalo explícitamente

## Output (formato exacto)

Cuando generes un skill, responde con este formato:

```
## Carpeta
.agent/skills/<nombre-del-skill>/

## SKILL.md

---
name: ...
description: ...
---

# <Título del skill>

## Cuándo usar este skill
- ...

## Inputs necesarios
- ...

## Workflow
1) ...
2) ...
3) ...

## Instrucciones
...

## Output (formato exacto)
...

## Recursos opcionales (solo si aportan valor)
- recursos/<archivo>.md
- scripts/<archivo>.sh
```

## Skills que puedes sugerir

Si el usuario está creando skills, sugiere ideas útiles:
- Skill de "estilo y marca"
- Skill de "planificar vídeos"
- Skill de "auditar landing"
- Skill de "debug de app"
- Skill de "responder emails con tono"
- Skill de "crear documentación"
- Skill de "revisar código"
