# Bitácora del trabajo de los agentes

Una fila por trabajo. Las más recientes, abajo. Si no sabes algo: «pendiente».
**Revisión humana** = tú has leído y comprobado el resultado (no solo lo ha ejecutado el agente).
Esta bitácora **hace de declaración de uso de IA** del módulo.

| Fecha | Agente y modelo | Qué pedí | Qué acepté o cambié | Dónde quedó | Revisión humana |
|---|---|---|---|---|---|
| 2026-11-13 | `documentador` con `opencode/big-pickle` | Investigar el sector editorial y de herramientas de lectura y escritura, y redactar el análisis y el estado del arte del TFG. | Se aceptó la estructura y se revisaron enlaces y cifras; se ajustaron el alcance del MVP y las decisiones técnicas. | `docs/01-analisis.md`, `docs/01b-sota.md` | Hecho |
| 2026-11-19 | `documentador` con `opencode/big-pickle` | Revisar la semana 1 con el modelo de `plantilla-proyecto` y añadir lo que faltaba según el tutor. | Se crearon `README.md`, `AGENTS.md`, `opencode.jsonc`, `.gitignore`, la carpeta `asistenciaIA/`, las licencias y una declaración de uso de IA. Se adaptaron los textos a ENTRE LÍNEAS. | `README.md`, `AGENTS.md`, `opencode.jsonc`, `.gitignore`, `asistenciaIA/`, `docs/declaracion-uso-ia.md`, `LICENSE`, `docs/LICENCIA-DOCS.md` | Hecho |
| 2026-11-19 | `documentador` con `opencode/big-pickle` | Generar los diagramas del análisis y del estado del arte para insertarlos en los documentos. | Se generaron fuentes `.mmd` y exportaciones PNG/SVG. Después se comprobó que la base del curso pide **Mermaid, no imágenes**: los documentos se pasaron a bloques Mermaid y las imágenes quedaron como exportación opcional. | `docs/diagramas/`, `docs/01-analisis.md`, `docs/01b-sota.md` | Hecho |
| 2026-11-19 | `documentador` con `opencode/big-pickle` | Revisar `semana-01-base`, completar la estructura de `.opencode/` y `asistenciaIA/` y restaurar la carpeta de diagramas. | Se añadieron `asistenciaIA/README.md`, `esquema-agentes.md`, `docs/como-trabajamos.md`, `diagramas/` y `esquemas/semana-01.md`; se adaptó esta bitácora y se actualizaron `AGENTS.md`, `opencode.jsonc` y `.gitignore`. | `.opencode/`, `asistenciaIA/`, `AGENTS.md`, `opencode.jsonc`, `.gitignore` | Hecho |
| 2026-11-20 | `guia` con `opencode/big-pickle` | Explicar cómo convertir la carpeta local en repositorio Git, enlazarla con el remoto existente y subir el contenido. | Se siguió la ruta segura: `git init`, `git remote add origin`, `git fetch`, `git reset --mixed origin/main` y `git branch -M main`; se revisó `git status` y se hizo commit y push. | Commit `6c88b99` en `.git/` y `origin/main`; `asistenciaIA/bitacora.md` (esta fila) | Hecho |

## Notas

- La IA se ha usado como **apoyo**: búsqueda, estructura, redacción y revisión. La responsabilidad del contenido y de las decisiones es de la alumna.
- Las fuentes citadas están en el apartado 9 de `docs/01-analisis.md` y en el apartado 7 de `docs/01b-sota.md`.
- No se han introducido claves, contraseñas ni datos personales en el chat.
- Si se usa otra herramienta (ChatGPT, Gemini, Copilot, etc.), se añade una fila con la misma estructura.
- La declaración oficial es **esta bitácora**. [`docs/declaracion-uso-ia.md`](../docs/declaracion-uso-ia.md) solo resume el alcance y enlaza aquí.
