---
name: doc-to-app
description: Convierte un documento (PDF/texto) en una mini-app web interactiva lista para abrir en preview. Úsalo cuando quieras pasar de "contenido" a "producto usable".
---

# Doc-to-App (Documento a Mini-App)

## Cuándo usar este skill

- Cuando tengas información en un PDF, texto o notas y quieras transformarla en una mini web navegable.
- Cuando necesites buscador, filtros y secciones claras en lugar de un documento estático.
- Cuando quieras algo listo para enseñar o compartir.

## Inputs necesarios

> Si falta alguno, **pregunta primero** antes de generar.

1. **Fuente** - PDF o texto pegado
2. **Tipo de app** - guía, catálogo, checklist, itinerario, etc.
3. **Prioridad** - "más visual" o "más práctica"
4. **Idioma y estilo** - claro, sencillo, sin jerga

## Reglas importantes

- **No devuelvas solo texto.** Debes crear archivos y una vista previa.
- **No sobrescribas nada.** Cada ejecución crea una carpeta nueva.
- **Móvil primero.** La app debe funcionar bien en móvil.
- **Sin frameworks.** HTML + CSS + JS vanilla únicamente.

## Estructura de salida (crear siempre)

Crea una carpeta nueva con nombre:
```
miniapp_<tema>_<YYYYMMDD_HHMM>/
├── index.html      ← La app interactiva
├── data.json       ← Datos estructurados extraídos
└── README.txt      ← Cómo abrirla y qué incluye
```

## Funcionalidades mínimas de la app

| Funcionalidad | Descripción |
|---------------|-------------|
| **Buscador** | Filtrar por texto en tiempo real |
| **Filtros** | Por categorías/etiquetas cuando tenga sentido |
| **Navegación** | Índice arriba o lateral por secciones |
| **Diseño** | Limpio, legible, responsive (móvil primero) |
| **Acciones** | "Copiar", "marcar hecho", "expandir/contraer" si aplica |

## Workflow (orden fijo)

### Paso 1: Leer y extraer
- Analizar el documento
- Identificar estructura: secciones, listas, tablas, puntos clave
- Detectar categorías o etiquetas naturales

### Paso 2: Estructurar datos
- Crear `data.json` con formato ordenado
- Incluir: id, título, contenido, categoría, etiquetas

### Paso 3: Generar la app
- Crear `index.html` que lea de `data.json`
- Sin frameworks (HTML + CSS + JS vanilla)
- Implementar buscador, filtros y navegación

### Paso 4: Validar
- [ ] Se ve bien en móvil
- [ ] El buscador funciona
- [ ] Los filtros funcionan
- [ ] No hay contenido roto o faltante
- [ ] README.txt explica cómo usar

### Paso 5: Entregar
- Crear la carpeta con todos los archivos
- Responder en chat con resumen

## Output (formato exacto)

### En archivos:

**Carpeta:** `miniapp_<tema>_<YYYYMMDD_HHMM>/`

**data.json:**
```json
{
  "titulo": "...",
  "descripcion": "...",
  "secciones": [
    {
      "id": "1",
      "titulo": "...",
      "contenido": "...",
      "categoria": "...",
      "etiquetas": ["...", "..."]
    }
  ]
}
```

**index.html:** App funcional con buscador, filtros, navegación.

**README.txt:** Instrucciones de uso.

---

### En chat (siempre responder con):

```
✅ Carpeta creada: miniapp_<tema>_<YYYYMMDD_HHMM>/

📂 Abre: miniapp_<tema>_<YYYYMMDD_HHMM>/index.html

📋 Resumen:
- Secciones: [lista]
- Funcionalidades: buscador, filtros, navegación
- Total items: [número]
```

---

## Manejo de errores

- Si el PDF no se puede leer → pide al usuario que pegue el texto.
- Si la estructura no está clara → pregunta qué secciones quiere.
- Si faltan categorías → sugiere unas basadas en el contenido.
