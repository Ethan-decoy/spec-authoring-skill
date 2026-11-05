# spec-authoring-skill · Guideline Authoring and Review

[中文](README.md) · [English](README.en.md)

Agent Skills for establishing proportionate shared conventions and thoroughly checking whether work follows them.

## Skills

| Skill | Purpose | Status |
| --- | --- | --- |
| [spec-authoring · Guideline Authoring](spec-authoring/SKILL.en.md) | Draft, revise, or assess the guidelines themselves, using proportionate constraints to clarify purpose, principles, and boundaries while preserving choice of methods | Released `v0.2.0` |
| [spec-review · Review Against Guidelines](spec-review/SKILL.en.md) | Check work against existing guidelines item by item, covering every applicable requirement and location and delivering conclusions in chat | Released `v0.2.0` |

Guideline Authoring applies wherever shared conventions are needed and does not prescribe fixed sections, steps, or output templates. Review Against Guidelines is complete when all applicable requirements have been checked; methods and the organization of results suit the task, with delivery in chat by default.

## Language

Chinese is the primary version for maintenance and validation. English translations help readers understand the instructions and are kept aligned with their respective Chinese originals. If their meanings differ, the Chinese originals take precedence. See the translations of [Guideline Authoring](spec-authoring/SKILL.en.md) and [Review Against Guidelines](spec-review/SKILL.en.md).

The installed entry point remains the Chinese `SKILL.md`, and the interface text remains in Chinese. You can specify the language of a task and its output. Providing an English translation does not mean that the effectiveness of English instructions has been validated.

## Installation

### Install with Codex

The two skills can be installed independently as needed.

To install Guideline Authoring, send this to Codex:

```text
$skill-installer install https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.0/spec-authoring
```

To install Review Against Guidelines:

```text
$skill-installer install https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.0/spec-review
```

These URLs are pinned to `v0.2.0`. To follow the latest source, replace `v0.2.0` with `main`.

### Manual installation

Download the archive for the skill you need from [GitHub Releases](https://github.com/Ethan-decoy/spec-authoring-skill/releases), extract it, and place the entire `spec-authoring` or `spec-review` folder in the skill directory used by your Agent Skills-compatible tool.

For Codex, use `~/.agents/skills/` for your user account, or `.agents/skills/` in the target project. Keep each skill in its own folder named after the skill, containing `SKILL.md`. If the interface does not update, restart the client. See the [official Codex skill documentation](https://learn.chatgpt.com/docs/build-skills). For other tools, consult their documentation for discovery and installation.

## Usage

To write or assess the conventions themselves:

```text
Use $spec-authoring to draft or revise the guidelines we need, based on the current purpose, context, and available material.
```

Provide the material you have and the problem you need to resolve. You do not need to fill out a fixed set of fields in advance.

To review work against existing guidelines:

```text
Use $spec-review to review the current work thoroughly against the applicable guidelines and explain the findings, evidence, and review limitations in chat.
```

## Contents and principles

Read the [Chinese original](spec-authoring/SKILL.md) or the [English translation](spec-authoring/SKILL.en.md). The skill distinguishes confirmed requirements, observed practices, facts, and suggestions, preserving their conditions of applicability and unresolved issues. A practice does not become binding simply because it exists. The guidelines contain usable conventions; research and revision records are kept separately according to their purpose.

Review Against Guidelines checks the source, applicable conditions, actual locations, and judgment for each requirement. Requirements that apply in several places are checked at every applicable location. It distinguishes evidence-supported compliance, deviations, non-applicability, insufficient evidence, and unchecked work. Results are delivered directly in chat without a separate coverage record or review document. Files for review material or revisions to the work are written only when the user explicitly requests those outputs or changes. Unresolved applicable requirements keep the review incomplete or its conclusion limited.

```text
spec-authoring/
├── SKILL.md
├── SKILL.en.md
├── LICENSE
└── agents/
    └── openai.yaml
spec-review/
├── SKILL.md
├── SKILL.en.md
├── LICENSE
└── agents/
    └── openai.yaml
```

The skill contains no executable scripts or external service dependencies.

## Validation and feedback

`v0.2.0` is publicly released and includes `spec-authoring` and `spec-review`. Both skills have a Chinese original and an English translation. The `spec-authoring` instructions are unchanged from `v0.1.1`; validation covers format checks and a small number of drafting checks using real material.

One static comparison of `spec-review` has been completed using a local controlled variant of real guidelines and note material, checking requirement coverage, repeated applicable locations, and the handling of unverified properties. The change to delivery in chat by default was checked in a separate focused trial; workspace file contents were identical before and after that review. Neither skill has demonstrated consistent improvement across tasks and models.

Use [Issues](https://github.com/Ethan-decoy/spec-authoring-skill/issues) to share your intended use, the behavior you observed, and judgments that need improvement. Remove private information before sharing material.

## Maintenance

See [AGENTS.md](AGENTS.md) for the project maintenance instructions, which are in Chinese. Private samples, research drafts, individual validation outputs, and local release preparation files stay in the Git-ignored `local_artifacts/` directory. They are excluded from the public source and installation archive. Reusable examples require permission before they are added to the distributed resources.

## License

[MIT](LICENSE).
