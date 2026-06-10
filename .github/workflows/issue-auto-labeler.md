---
description: Etiqueta automáticamente issues nuevos basándose en su contenido
on:
  issues:
    types: [opened]
engine: copilot
---

# Issue Auto-Labeler

Cuando se crea un nuevo issue, analiza su título y descripción para asignar etiquetas apropiadas.

## Tareas:

1. Lee el título y el cuerpo del issue
2. Identifica palabras clave:
   - Si menciona "bug", "error", "falla" → etiqueta "bug"
   - Si menciona "feature", "mejora", "nueva funcionalidad" → etiqueta "enhancement"
   - Si menciona "documentación", "docs", "readme" → etiqueta "documentation"
   - Si menciona "pregunta", "duda", "ayuda" → etiqueta "question"
3. Agrega las etiquetas correspondientes al issue
4. Comenta en el issue: "✅ Issue etiquetado automáticamente como: [lista de etiquetas]"
