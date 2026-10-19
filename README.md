# Before Launch 🚀 / Antes del Lanzamiento 🚀

Pre-launch verification project for any website. The rules live in **[`RULES.md`](./RULES.md)**; this README is only the documentation.

Proyecto de verificación previa al lanzamiento de cualquier sitio web. Las reglas viven en **[`RULES.md`](./RULES.md)**; este README es solo la documentación.

> 📖 **[English](#-english)** · **[Español](#-español)**

---

## 🇬🇧 English

### What is this?

A single machine-readable checklist (`RULES.md`) with the rules you must verify **before taking a site to production**, written bilingually (EN/ES) so both the agent and the client can read it.

### Structure

| File | Purpose |
|---|---|
| `README.md` | Documentation: what the project is, how to use it (this file) |
| `RULES.md` | The rules: the actual checklist to verify before launch |

### How an agent should use it

1. Read `RULES.md` top to bottom.
2. For each rule, **verify it with real evidence** (run the build, open the URL, run Lighthouse, check headers…). Never tick a box from assumption.
3. Tick `- [x]` only when the rule passes.
4. Apply the **Launch Gate** (bottom of `RULES.md`):
   - `BLOCKER` (sections 1, 4, 5, 10): a single failure means **no launch**.
   - `MAJOR` (sections 2, 3, 6, 7, 9): must be fixed before launch.
   - `MINOR` (section 8): fix within 48h after launch.
5. Report: list of passed rules, failed rules with severity, and a final `LAUNCH APPROVED` / `NO LAUNCH` verdict.

### How a human should use it

- Work through the checklist before every production deploy.
- Keep the box unchecked until you can demonstrate the fix.
- Sign off in the table below only when every `BLOCKER` and `MAJOR` rule is checked.

### Final sign-off / Aprobación final

| Role / Rol | Name / Nombre | Date / Fecha |
|---|---|---|
| Developer / Desarrollador |  |  |
| Designer / Diseñador |  |  |
| QA |  |  |
| Owner / Cliente |  |  |

---

## 🇪🇸 Español

### ¿Qué es esto?

Una única lista legible por máquina (`RULES.md`) con las reglas que debes verificar **antes de llevar un sitio a producción**, escrita en bilingüe (EN/ES) para que tanto el agente como el cliente puedan leerla.

### Estructura

| Archivo | Propósito |
|---|---|
| `README.md` | Documentación: qué es el proyecto, cómo usarlo (este archivo) |
| `RULES.md` | Las reglas: el checklist real a verificar antes del lanzamiento |

### Cómo debe usarlo un agente

1. Leer `RULES.md` de arriba a abajo.
2. Verificar cada regla con **evidencia real** (ejecutar el build, abrir la URL, correr Lighthouse, revisar cabeceras…). Nunca marcar una casilla por suposición.
3. Marcar `- [x]` solo cuando la regla pasa.
4. Aplicar la **Launch Gate** (final de `RULES.md`):
   - `BLOCKER` (secciones 1, 4, 5, 10): un solo fallo significa **no lanzar**.
   - `MAJOR` (secciones 2, 3, 6, 7, 9): corregir antes de lanzar.
   - `MINOR` (sección 8): corregir en 48h tras el lanzamiento.
5. Reportar: reglas aprobadas, reglas fallidas con severidad y veredicto final `LAUNCH APPROVED` / `NO LAUNCH`.

### Cómo debe usarlo una persona

- Recorrer el checklist antes de cada despliegue a producción.
- No marcar la casilla hasta poder demostrar la corrección.
- Firmar en la tabla solo cuando todas las reglas `BLOCKER` y `MAJOR` estén marcadas.

---

### Changelog

| Date | Change |
|---|---|
| 2026-10-19 | Initial bilingual checklist |
| 2026-10-19 | Split docs (`README.md`) from rules (`RULES.md`) |
