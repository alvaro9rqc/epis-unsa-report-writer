---
name: epis-unsa-report-writer
description: Guidelines and best practices for writing academic and laboratory reports in Typst for EPIS-UNSA (Escuela Profesional de Ingeniería de Sistemas - Universidad Nacional de San Agustín).
metadata:
  language: "es"
  organization: "EPIS-UNSA"
  author: "skills-dev"
  version: "1.0.0"
---

## General Guidelines

- When referencing code, figures, tables, code listings, images, or similar elements, use Typst's built-in referencing system (e.g., `@figure`) instead of manual references.

- Dedicated snippet directories (e.g., `src/lst/` or `code/`) are reserved **only** for code snippets included in the report. Do **not** place the project's source code there.

- Prefer fenced code blocks using three backticks (```) when inserting code examples (do not forget to use align to center it or figure to list them).

- Do **not** manually number section headings. For example, avoid writing `== 2.1 Header`; Typst automatically handles section numbering.

- Maintain the correct heading hierarchy. Do not skip heading levels or use inconsistent nesting.

- Use the `include` statement to organize the report into multiple files. Prefer a modular structure over large monolithic files.

- Write concise paragraphs and express ideas directly. Avoid unnecessary words or overly long explanations.

  - For example:

    - Bad content:

      > ### II. DESCRIPCIÓN DEL PROCEDIMIENTO REALIZADO EN LA PRÁCTICA
      >
      > 1. **Instalación y Configuración del Entorno de Gestión de Cambios:**
      >
      > * Se desplegó y configuró una herramienta de gestión de incidencias y cambios (se utilizó **Scarab / Redmine** en contenedor Docker).
      >
      > * Se definieron los roles dentro del sistema: *Solicitante (Cliente/Analista)*, *Comité de Control de Cambios (CCB / Project Manager)*, *Desarrollador/Arquitecto Distribuido* y *QA Tester*.
      >
      > 2. **Análisis del Diagrama de Flujo del Proceso de Gestión de Cambios:**
      >
      > * Se revisó el flujo estandarizado descrito en las buenas prácticas (Anexo 21 / ITIL / RUP):
      >
      >   1. **Identificación y Registro:** Creación de la Solicitud de Cambio (CR).
      >   2. **Evaluación de Impacto:** Análisis técnico (costo, esfuerzo, riesgos en la arquitectura distribuida, afectación a nodos).
      >   3. **Decisión del Comité (CCB):** Aprobación, rechazo, postergación o solicitud de mayor información.
      >   4. **Implementación:** Asignación al equipo de desarrollo y modificación de ECSs.
      >   5. **Verificación y Pruebas:** Validación de calidad (QA) e integración continua.
      >   6. **Cierre y Despliegue:** Actualización de la línea base (*baseline*) y notificación a los involucrados.

      *This content is wrong because it uses too many bullets and numbered lists, which is a bad pattern. It also uses unnecessary words, and this report should be direct.*

    - Correct content (the above fixed):

      > ### DESCRIPCIÓN DEL PROCEDIMIENTO REALIZADO EN LA PRÁCTICA
      >
      > 1. **Instalación y Configuración del Entorno de Gestión de Cambios:**
      >
      > Se desplegó y configuró una herramienta de gestión de incidencias y cambios usando Scarab y Redmine en Docker. Luego se definieron los siguientes roles: Solicitante (Cliente/Analista), Comité de Control de Cambios (CCB / Project Manager), Desarrollador/Arquitecto Distribuido y QA Tester.
      >
      > 2. **Análisis del Diagrama de Flujo del Proceso de Gestión de Cambios:**
      >
      > * Se revisó el flujo estandarizado descrito en el Anexo 21 / ITIL / RUP:
      >
      >   1. Identificación y Registro: Creación de la Solicitud de Cambio (CR).
      >   2. Evaluación de Impacto: Análisis técnico (costo, esfuerzo, riesgos, etc.).
      >   3. Decisión del Comité (CCB): Aprobación, rechazo, postergación o solicitud de mayor información.
      >   4. Implementación: Asignación al equipo de desarrollo y modificación de ECSs.
      >   5. Verificación y Pruebas: Validación de calidad (QA) e integración continua.
      >   6. Cierre y Despliegue: Actualización de la línea base (*baseline*) y notificación a los involucrados.

      *Note that in the first part, the bullet list has been replaced by a paragraph, which is more professional. Later, several parentheses have been removed because that information was needed to specify the content, and there were too many parentheses used.*

  - Here you have another example:

    - Note that the writing style is more direct, avoids using several connectors, does not abuse the **bold** style, does not use several parentheses, and does not use several adjectives.
    - Bad:

      > Cuando se abordan sistemas con alta variabilidad, múltiples componentes distribuidos o requisitos no funcionales estrictos (seguridad, rendimiento, alta disponibilidad), el costo de un cambio no planificado en etapas avanzadas puede multiplicar hasta por 100x el costo de haberlo evaluado preliminarmente. Por tanto, invertir hasta un 15% en análisis de impacto, reuniones del CCB, actualización de la trazabilidad y pruebas de regresión resulta ser altamente rentable (*prevención vs. corrección*).

    - Good:

      > Ante sistemas con alta variabilidad, componentes distribuidos o requisitos funcionales no estrictos, el costo en etapas avanzadas puede ser muy superior al haberlo evaluado preliminarmente. Por otro lado, según el análisis, es más rentable si es que se invierte un 15% en análisis de impacto, reuniones del CCB, trazabilidad y pruebas de regresión.

- Follow the formatting conventions defined by the report template and keep the style consistent throughout the document. If the user gives you a structure for the report, follow it; or if the report suggests or has a structure or sequence of activities, follow that structure. For example, if the report has two main parts, it is suggested that the written report also have them, and if inside those activities the report suggests a sequence of steps, it is also suggested that the written report also have headers following that structure. However, only use up to third-level headers—avoid using 4th level and beyond.

- The suggested flow is the following:

  - First, write a fast report (do not compile it yet). In this stage, you should just preview whether all the important content is included in the laboratory and evaluate if the evaluation criteria related to the activity itself have been addressed.
  - Later, verify whether the rules above have been met: first for the syntax, second for the writing style described above, and finally for coherence, adequacy, and cohesion.
