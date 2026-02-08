# Open Circle Agent Skills

A collection of [Agent Skills](https://agentskills.io) for [Open Circle](https://opencircle.dev) projects. These skills help AI agents define how schema definitions, validation logic, and form behavior are handled with Valibot, Formisch, and other ecosystem tools. 

## What are Agent Skills?

Agent Skills are a lightweight, open format for extending AI agent capabilities with specialized knowledge and workflows. Each skill is a folder containing a `SKILL.md` file with metadata and instructions that help AI agents understand how to use specific tools and libraries.

Learn more at [agentskills.io](https://agentskills.io)

## Purpose

These skills provide rules for:

* Defining and validating schemas with Valibot
* Handling form state and transitions with Formisch

Without these skills, schema structure and form behavior are not defined for the agent.

## Who this is for

This repository is for developers who are:

* Building agents that generate, validate, or reason about structured data or forms
* Using or evaluating Valibot or Formisch in agent workflows
* Wanting rules for how schema and form logic is applied by the agent

This requires an agent runtime that loads instructions from `SKILL.md` files.

## Skills included

| Skill             | Purpose                          | When to use                                              |
| ----------------- | -------------------------------- | -------------------------------------------------------- |
| `valibot-usage/`  | Schema definition and validation | Validating data structures, API responses, or user input |
| `formisch-usage/` | Form state handling              | Managing multi-step forms or structured data collection  |

## Installation

Install the skills using the CLI:
```bash
npx skills add open-circle/agent-skills
npx add-skill open-circle/agent-skills
```

Or copy individual skill folders into your project's `.skills/` directory.

## Usage

1. The agent loads all available skills from the skills directory at startup.
2. Instructions are read from each skill's `SKILL.md` file.
3. During schema definition, validation, and form handling, the agent applies instructions.

No prompt changes are required.

## Skill structure

Each skill folder contains:

* `SKILL.md` – Instructions and metadata for the agent
* `references/` – Optional supporting documentation
* `scripts/` – Optional executable code
* `assets/` – Optional templates or examples

---

## FAQ

**Is this only for Open Circle projects?**
No. Skills can be used with any agent runtime that loads instructions from `SKILL.md` files.

**Do I need to modify my prompts?**
No. Skills are applied automatically by the agent runtime.

**Can I use only one skill?**
Yes. Install individual skills or ignore unused ones.

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## About Open Circle

[Open Circle](https://opencircle.dev) is a GitHub organization serving as a shared home for open-source projects that share a philosophy around modularity, type safety, and developer experience.

### Projects

- **[Valibot](https://valibot.dev)** — The modular and type safe schema library for validating structural data
- **[Formisch](https://formisch.dev/)** — The modular and type-safe form library for any framework

## License

This repository is licensed under the [MIT License](LICENSE.md).
