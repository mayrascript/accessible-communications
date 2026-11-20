# Accessible Communications

Use this Agent Skill to draft and review accessible emails, announcements, forms, schedules, graphics, slides, and videos. It includes a practical checklist for in-person, virtual, and hybrid tech events, with a focus on Deaf and hard-of-hearing participants. The skill is documented in English and drafts audience-facing copy in Spanish by default unless you request another language.

## Install

From your project, run [Skills CLI](https://github.com/vercel-labs/skills):

```sh
npx skills add mayrascript/accessible-communications --skill accessible-communications
```

Choose your agent when prompted, or pass `-a codex`. Add `-g` to install for your user. Use `npx skills add mayrascript/accessible-communications --list` to discover the skill without installing it.

With [GitHub CLI](https://cli.github.com/manual/gh_skill_install) (preview):

```sh
gh skill install mayrascript/accessible-communications accessible-communications --agent codex --scope project
```

**Built-in Codex installer:** Ask Codex to use `$skill-installer` with https://github.com/mayrascript/accessible-communications/tree/main/accessible-communications. Invoke it with `$accessible-communications`.

**Manual installation:** Copy [the whole skill folder](accessible-communications/) into your agent's skill directory. For assistants without [Agent Skills](https://agentskills.io/specification) support, paste [`SKILL.md`](accessible-communications/SKILL.md) as task instructions. Add the [event checklist](accessible-communications/references/events.md) when planning, auditing, or coordinating an event.

**Upgrading from v1:** Install the new skill and retire the old `accesibilidad-comunicaciones` copy to avoid two active versions. Update your invocation to `$accessible-communications` and any installation commands to the new repository and skill names. The [v1.0.0 release](https://github.com/mayrascript/accessible-communications/releases/tag/v1.0.0) remains available.

## Credits and license

Adapted from [*Guía de accesibilidad para eventos tech*](https://github.com/tech-andgar/guia-accesibilidad-tech) by Andrés García (`tech-andgar`) and contributors, under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). This adaptation summarizes the operational checklist, extends it to other communication channels, and translates the instructions into English. See [LICENSE](LICENSE).

Editorial reference: [Writing for Agents, AI Hero](https://www.aihero.dev/skills-writing-for-agents).
