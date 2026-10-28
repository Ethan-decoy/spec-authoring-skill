# spec-authoring · Guideline Authoring

[中文](README.md) · [English](README.en.md)

An Agent Skill for drafting, revising, and reviewing guidelines based on the actual purpose, context, and available material. It uses proportionate constraints to establish shared understanding and a basis for judgment, while preserving as much choice of methods as possible within the purpose, principles, and boundaries.

The skill applies wherever shared conventions are needed. It does not prescribe fixed sections, steps, or output templates. It is not needed when a task only involves following existing guidelines.

## Language

Chinese is the primary version for maintenance and validation. The [English skill translation](spec-authoring/SKILL.en.md) helps readers understand the instructions and is kept aligned with the [Chinese original](spec-authoring/SKILL.md). If their meanings differ, the Chinese original takes precedence.

The installed entry point remains the Chinese `SKILL.md`, and the interface text remains in Chinese. You can specify the language of a task and its output. Providing an English translation does not mean that the effectiveness of English instructions has been validated.

## Installation

### Install with Codex

Send this to Codex:

```text
$skill-installer install https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.1.1/spec-authoring
```

This URL is pinned to `v0.1.1`. To follow the latest source, replace `v0.1.1` with `main`.

### Manual installation

Download the skill archive from [GitHub Releases](https://github.com/Ethan-decoy/spec-authoring-skill/releases), extract it, and place the entire `spec-authoring` folder in the skill directory used by your Agent Skills-compatible tool.

For Codex, use `~/.agents/skills/spec-authoring/` for your user account, or `.agents/skills/spec-authoring/` in the target project. Confirm that the installed folder contains `SKILL.md`. If the interface does not update, restart the client. See the [official Codex skill documentation](https://learn.chatgpt.com/docs/build-skills). For other tools, consult their documentation for discovery and installation.

## Usage

```text
Use $spec-authoring to draft or revise the guidelines we need, based on the current purpose, context, and available material.
```

Provide the material you have and the problem you need to resolve. You do not need to fill out a fixed set of fields in advance.

## Contents and principles

Read the [Chinese original](spec-authoring/SKILL.md) or the [English translation](spec-authoring/SKILL.en.md). The skill distinguishes confirmed requirements, observed practices, facts, and suggestions, preserving their conditions of applicability and unresolved issues. A practice does not become binding simply because it exists. The guidelines contain usable conventions; research and revision records are kept separately according to their purpose.

```text
spec-authoring/
├── SKILL.md
├── SKILL.en.md
├── LICENSE
└── agents/
    └── openai.yaml
```

The skill contains no executable scripts or external service dependencies.

## Trial use and feedback

The current version, `v0.1.1`, is a public preview. It adds English reading material to `v0.1.0`; the Chinese skill instructions are unchanged. Validation so far covers format checks and a small number of drafting checks using real material. Consistent improvement across tasks and models has not been demonstrated.

Use [Issues](https://github.com/Ethan-decoy/spec-authoring-skill/issues) to share your intended use, the behavior you observed, and judgments that need improvement. Remove private information before sharing material.

## Maintenance

See [AGENTS.md](AGENTS.md) for the project maintenance instructions, which are in Chinese. Private samples, research drafts, individual validation outputs, and local release preparation files stay in the Git-ignored `local_artifacts/` directory. They are excluded from the public source and installation archive. Reusable examples require permission before they are added to the distributed resources.

## License

[MIT](LICENSE).
