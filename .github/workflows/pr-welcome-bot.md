---
description: Da la bienvenida a nuevos pull requests con información útil
on:
  pull_request:
    types: [opened]
engine: copilot
---

# PR Welcome Bot

Cuando se abre un nuevo pull request, analiza su contenido y da una bienvenida personalizada.

## Análisis:

1. Verifica si el autor es un contribuidor nuevo (primera PR al repo)
2. Cuenta el número de archivos modificados
3. Identifica el tipo de cambios:
   - Código (archivos .js, .ts, .py, etc.)
   - Documentación (archivos .md)
   - Configuración (archivos .json, .yml, etc.)

## Respuesta:

Agrega un comentario al PR con el siguiente formato:

```markdown
👋 ¡Hola @[autor]!

[Si es contribuidor nuevo:]
🎉 ¡Gracias por tu primera contribución a este repositorio!

📊 **Resumen del PR:**
- 📁 Archivos modificados: X
- 📝 Tipo de cambios: [código/documentación/configuración]

✅ **Próximos pasos:**
- Los maintainers revisarán tu PR pronto
- Asegúrate de que todos los checks pasen
- Responde a cualquier feedback de la revisión

---
*Mensaje automático de PR Welcome Bot* 🤖
```
