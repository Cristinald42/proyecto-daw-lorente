# ENTRE LÍNEAS

**Una frase:** aplicación web para lectores y escritores que reúne la biblioteca personal, el diario de lectura y los proyectos literarios en un mismo espacio, de modo que lo que se lee pueda alimentar lo que se escribe.

## Estado

| Fase | Estado |
|---|---|
| Análisis | En curso — H1 el 26-nov-2026 |
| Diseño | Pendiente — H2 el 21-ene-2027 |
| Planificación | Pendiente |
| Implementación | Pendiente — MVP el 31-mar-2027 |
| Pruebas | Pendiente |
| Despliegue | Pendiente |
| Seguimiento y cierre | Pendiente |

## Documentación

- [`docs/00-documentoInicio.md`](docs/00-documentoInicio.md) — propuesta y alcance inicial.
- [`docs/01-analisis.md`](docs/01-analisis.md) — sector, necesidades, requisitos y plan de trabajo.
- [`docs/01b-sota.md`](docs/01b-sota.md) — estado del arte, modelos de negocio y viabilidad técnica.
- [`docs/declaracion-uso-ia.md`](docs/declaracion-uso-ia.md) — resumen de la declaración de uso de IA.
- [`asistenciaIA/bitacora.md`](asistenciaIA/bitacora.md) — declaración oficial y registro de las sesiones con IA.
- [`asistenciaIA/README.md`](asistenciaIA/README.md) — qué hay en la carpeta de asistencia.
- [`.opencode/README.md`](.opencode/README.md) — agentes, comandos y skills del proyecto.

Los documentos de diseño, planificación, seguimiento y memoria se añadirán en H2 y H3.

## Estructura del repositorio

```text
.
├── docs/                  Documentación del TFG
│   ├── decisiones/        Registros de decisiones técnicas (ADR)
│   └── diagramas/         Fuentes Mermaid (.mmd) y exportaciones opcionales
├── .opencode/             Agentes, comandos, skills y su versionado
├── asistenciaIA/          Bitácora y documentación del trabajo con IA
│   ├── bitacora.md        Declaración oficial y registro de sesiones
│   ├── esquema-agentes.md Esquema vigente de agentes
│   ├── docs/              Cómo trabajamos
│   ├── diagramas/         Diagramas Mermaid del ciclo de trabajo
│   └── esquemas/          Fotos semanales del esquema de agentes
├── src/                   Código de la aplicación (pendiente)
├── tests/                 Pruebas automatizadas (pendiente)
├── AGENTS.md              Instrucciones para asistentes de IA
├── opencode.jsonc         Configuración de OpenCode
├── .gitignore
├── LICENSE
└── README.md
```

## Diagramas

Los diagramas se escriben en **Mermaid** dentro de los documentos. [`docs/diagramas/`](docs/diagramas/) conserva las fuentes `.mmd` y algunas exportaciones opcionales; [`asistenciaIA/diagramas/`](asistenciaIA/diagramas/) explica el ciclo semanal y la validación de la estructura.

## Tecnologías previstas

- **Backend:** Java 21, Spring Boot 3.x, Spring Security, Spring Data JPA.
- **Base de datos:** MySQL 8.4 LTS con migraciones Flyway.
- **Frontend:** Thymeleaf, Bootstrap 5, HTML, CSS y JavaScript.
- **Pruebas:** JUnit 5, Mockito, Testcontainers y Playwright.
- **Despliegue:** Docker Compose, Nginx y un VPS.

## Cómo ejecutarlo

Pendiente de la fase de implementación. Cuando exista el proyecto se documentarán aquí los pasos:

```bash
# 1. Crear la base de datos y configurar las variables de entorno
# 2. Arrancar la aplicación
./mvnw spring-boot:run

# 3. O con Docker Compose
docker compose up --build
```

No se subirán claves ni datos personales al repositorio. La configuración local se guardará en `.env`, que está ignorado por Git.

## Uso de IA

La IA se utiliza como apoyo para buscar, estructurar y revisar, nunca para sustituir la autoría del trabajo. Cada sesión queda registrada en [`asistenciaIA/bitacora.md`](asistenciaIA/bitacora.md), que hace de declaración oficial de uso de IA. [`docs/declaracion-uso-ia.md`](docs/declaracion-uso-ia.md) solo resume el alcance y enlaza a la bitácora. No se introducen datos personales, claves ni información confidencial en las herramientas.

## Autoría

Cristina Lorente Díaz. Proyecto intermodular de Desarrollo de Aplicaciones Web (0616), CIFP Sectores Industriales y Servicios, curso 2026-27.

## Licencia

Código: [MIT](LICENSE). Documentación: [CC BY 4.0](docs/LICENCIA-DOCS.md).
