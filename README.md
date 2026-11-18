# dev-implementador-autonomo

Skill para delegar el desarrollo completo de una feature: el agente investiga referentes en internet, decide la arquitectura con evidencia, implementa el código y lo verifica con tests. Un único checkpoint de aprobación antes de escribir código. Funciona con cualquier agente que cargue skills por carpeta.

## Qué garantiza

- **Investigación primero**: qué se ha implementado antes y qué partes sirven, con enlaces verificables.
- **Decisiones con origen**: cada decisión lleva `[BRIEF]`, `[REPO]`, `[REFERENTE]` o `[DECISIÓN]`; nada se inventa.
- **Un único checkpoint**: investigación + arquitectura + plan de pruebas en un solo mensaje; después, APROBADO y a implementar.
- **Cero inferencias silenciosas**: lo que no tenga origen se pregunta, agrupado, una sola vez.
- **Tests de verdad**: features en Python se verifican con la skill `test-feature`; el resto, con la infraestructura del repositorio.
- **Verificación honesta**: comandos y resultados reales; los fallos se reportan, no se ocultan.

## Instalación

Clona el repositorio en la carpeta de skills del agente (OpenCode: `~/.config/opencode/skills/`; otros agentes: la que indique su documentación) y recarga la lista de skills.

## Uso

```text
Usa dev-implementador-autonomo.

Quiero un acortador de URLs interno en FastAPI y PostgreSQL, con rate limit y expiración. Hazlo todo: investiga, implementa y testea. No tengo tiempo para decidir la arquitectura.
```

La skill pedirá solo el brief que falte, investigará y presentará todo en el checkpoint único antes de escribir código.

## Flujo

Fase 0 brief → Fase 1 investigación → Fase 2 arquitectura ensamblada → Checkpoint único (APROBADO) → Fase 3 implementación por lotes → Fase 4 tests → Fase 5 cierre.

## Skill hermana

Si en cambio quieres ser tú quien decide la arquitectura y que el agente solo implemente, usa `dev-arquitecto-software`.

## Pruebas

Lee `PRUEBAS.md`. Incluye prompts listos para copiar en otra instancia o agente y señales de éxito y fallo.

## Licencia

GNU General Public License v3.0. Ver [LICENSE](LICENSE).
