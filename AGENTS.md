# AGENTS.md — Instrucciones para asistentes de IA

> Este archivo lo leen los asistentes de IA que trabajan en el repositorio. No sustituye a la documentación del TFG: la fuente de verdad son `docs/00-documentoInicio.md`, `docs/01-analisis.md` y `docs/01b-sota.md`.

## 1. Proyecto

**ENTRE LÍNEAS** es una aplicación web de uso personal para lectores que también escriben. Reúne tres bloques conectados:

1. **Biblioteca y seguimiento de lectura:** libros, estados, progreso, sesiones, valoraciones y estadísticas.
2. **Diario literario:** entradas, citas, anotaciones y emociones asociadas a una lectura.
3. **Proyectos literarios:** obras, capítulos, escenas, personajes, escenarios y cronología.

No es una red social, ni un marketplace, ni una aplicación móvil o de escritorio. El producto se ejecuta en el navegador y se adapta a distintos tamaños de pantalla.

## 2. Fase actual

- **H1 (26-nov-2026):** análisis y estado del arte.
- **H2 (21-ene-2027):** diseño funcional y técnico, modelo de datos y prototipo.
- **MVP (31-mar-2027):** versión funcional desplegada.
- **Entrega final:** junio de 2027.

No adelantar código de fases posteriores sin que la alumna lo pida.

## 3. Stack previsto

| Capa | Tecnología |
|---|---|
| Lenguaje | Java 21 (LTS) |
| Backend | Spring Boot 3.x, Spring Web, Spring Data JPA, Spring Security |
| Vistas | Thymeleaf + Bootstrap 5 |
| Base de datos | MySQL 8.4 LTS |
| Migraciones | Flyway |
| Pruebas | JUnit 5, Mockito, Testcontainers, Playwright |
| Despliegue | Docker Compose, Nginx, VPS |
| Control de versiones | Git y GitHub |

## 4. Estructura

```text
docs/                  Documentación del TFG y diagramas
  decisiones/          Registros de decisiones (ADR)
  diagramas/           Fuentes Mermaid (.mmd) y exportaciones opcionales
.opencode/             Agentes, comandos, skills y su versionado
asistenciaIA/          Bitácora, esquema de agentes, documentación y diagramas
  docs/                Cómo trabajamos
  diagramas/           Diagramas Mermaid del trabajo con agentes
  esquemas/            Fotos semanales del esquema de agentes
src/                   Código de la aplicación (pendiente)
tests/                 Pruebas automatizadas (pendiente)
AGENTS.md              Estas instrucciones
opencode.jsonc         Permisos, modelo y agente por defecto
```

## 5. Reglas de trabajo con la persona

- Responde **en español**, con frases cortas y sin jerga innecesaria.
- **Un paso cada vez.** No escribas apartados completos de `docs/` sin que la persona lo confirme.
- **No califiques.** La nota es del profesor. Puedes decir qué casillas de «Hecho cuando» se cumplen, no si «está bien» o «mal».
- **No inventes** datos, cifras, empresas, normas ni enlaces. Si no puedes comprobar algo, dilo.
- Todo dato externo lleva **enlace, fecha de acceso (AAAA-MM-DD) y estado** (`leído` / `sin leer`).
- **No reescribas la documentación de la alumna sin avisar.** Propón cambios y explica por qué.
- Si algo no se sabe, escribe **«pendiente»** y el motivo; no rellenes con texto inventado.

## 6. Reglas que no se negocian

1. **Nada de datos personales reales.** Ni en el código, ni en las pruebas, ni en las capturas, ni en los documentos. Solo datos ficticios.
2. **Nada de secretos.** No escribir contraseñas, claves, tokens ni cadenas de conexión reales. Usar `.env` y variables de entorno.
3. **El repositorio es público.** Todo lo que se sube lo puede leer cualquiera.
4. **No copiar código sin licencia.** Toda dependencia debe tener una licencia compatible y su atribución.
5. **No inventar fuentes, cifras ni funcionalidades.** Si algo no se ha comprobado, se dice.
6. **Registrar el uso de IA.** Cada sesión se anota en `asistenciaIA/bitacora.md`. Esa bitácora hace de declaración de uso de IA del módulo.
7. **Diagramas en Mermaid, no imágenes.** Los diagramas se escriben como bloques `mermaid` dentro del Markdown. Las imágenes de `docs/diagramas/` son solo exportaciones opcionales.
8. **Lo irreversible lo ejecuta la persona.** No ejecutes `git push`, `git reset` ni borrados. No leas `.env`.
9. **Accesibilidad y privacidad desde el diseño.** WCAG 2.2 AA como referencia y minimización de datos.

## 7. OpenCode en este proyecto

- `opencode.jsonc` define el modelo gratuito, el agente por defecto (`guia`) y los permisos.
- `.opencode/agents/guia.md` es **solo lectura**: acompaña y comprueba.
- `.opencode/agents/documentador.md` es el único que puede escribir, y solo en `docs/`, `README.md` y `asistenciaIA/`, con confirmación.
- `.opencode/commands/` contiene `/paso`, `/comprobar`, `/documentar`, `/validar` y `/bitacora`.
- `.opencode/skills/` contiene los procedimientos por paso y las skills de control.
- La lista de versiones está en `.opencode/MANIFIESTO.md` y los cambios en `.opencode/CHANGELOG.md`.

## 8. Comandos

Cuando exista el proyecto Maven:

```bash
./mvnw spring-boot:run          # arrancar en local
./mvnw test                     # pruebas unitarias y de integración
./mvnw verify                   # pruebas + análisis de calidad
docker compose up --build       # entorno completo
```

## 9. Convenciones

- **Idioma:** interfaz, documentación y mensajes de error en español; nombres de clases, tablas y variables en inglés.
- **Paquete base:** `com.cristinald42.entrelineas`.
- **Commits:** `tipo(alcance): descripción` — por ejemplo, `feat(biblioteca): alta de libros`.
- **Ramas:** `main` estable; una rama por funcionalidad o corrección.
- **Estilo:** código claro antes que código ingenioso; sin dependencias nuevas sin justificar.
- **Documentación:** cada decisión técnica importante se registra en `docs/decisiones/`.

## 10. Criterio de entrega

Una tarea está terminada cuando:

- el código compila y las pruebas pasan;
- no hay secretos ni datos personales;
- la documentación afectada está actualizada;
- el cambio se ha registrado en `asistenciaIA/bitacora.md` si se ha usado IA;
- la alumna puede explicar qué hace y por qué.
