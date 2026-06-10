---
description: Genera un resumen diario de la actividad del repositorio
on:
  schedule:
    - cron: '0 9 * * *'  # Todos los días a las 9:00 AM UTC
  workflow_dispatch:  # También permite ejecución manual
engine: copilot
---

# Daily Repo Summary

Crea un resumen diario de la actividad del repositorio.

## Análisis a realizar:

1. **Issues**: Contar issues abiertos hoy, cerrados hoy, total de issues abiertos
2. **Pull Requests**: Contar PRs abiertos hoy, mergeados hoy, total de PRs abiertos
3. **Commits**: Contar commits del día
4. **Top Contributors**: Listar los 3 usuarios más activos del día

## Output:

Crea un issue con título: "📊 Resumen Diario - [fecha actual]"

Contenido:
```
# Resumen de Actividad - [fecha]

## 📋 Issues
- Nuevos hoy: X
- Cerrados hoy: Y
- Total abiertos: Z

## 🔀 Pull Requests
- Nuevos hoy: X
- Mergeados hoy: Y
- Total abiertos: Z

## 💻 Commits
- Total del día: X

## 🌟 Top Contributors del día
1. @usuario1
2. @usuario2
3. @usuario3

---
*Generado automáticamente por Daily Repo Summary*
```
