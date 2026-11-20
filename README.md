# Accesibilidad en comunicaciones

## Instalar

Con [Skills CLI](https://github.com/vercel-labs/skills), desde tu proyecto:

```sh
npx skills add mayrascript/accesibilidad-comunicaciones --skill accesibilidad-comunicaciones
```

Selecciona tu agente. Añade `-g` para instalar para tu usuario, o `-a codex` para elegir Codex. Para ver qué se ofrece sin instalar, ejecuta `npx skills add mayrascript/accesibilidad-comunicaciones --list`.

Con [GitHub CLI](https://cli.github.com/manual/gh_skill_install) (función en vista previa):

```sh
gh skill install mayrascript/accesibilidad-comunicaciones accesibilidad-comunicaciones --agent codex --scope project
```

**Instalador de Codex:** pídele a Codex: «Usa `$skill-installer` para instalar https://github.com/mayrascript/accesibilidad-comunicaciones/tree/main/accesibilidad-comunicaciones». Luego invoca `$accesibilidad-comunicaciones` al revisar un material.

**Instalación manual:** copia [la carpeta del skill](accesibilidad-comunicaciones/) completa al directorio de skills de tu agente. Sigue el [estándar Agent Skills](https://agentskills.io/specification). Si tu asistente no admite skills, pega [`SKILL.md`](accesibilidad-comunicaciones/SKILL.md) como instrucciones. Si vas a coordinar o auditar un evento, adjunta también [el checklist](accesibilidad-comunicaciones/references/eventos.md).

## Créditos y licencia

Adaptado de la [Guía de accesibilidad para eventos tech](https://github.com/tech-andgar/guia-accesibilidad-tech), de Andrés García (`tech-andgar`) y colaboradores, bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). La adaptación resume el checklist operativo y amplía las pautas a otros canales de comunicación. Consulta [LICENSE](LICENSE).

Referencia editorial: [Writing for Agents, AI Hero](https://www.aihero.dev/skills-writing-for-agents).
