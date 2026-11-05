# spec-authoring-skill · Guideline Authoring and Review

[中文](README.md) · [English](README.en.md)

Agent Skills for building guidelines and reviewing existing material against applicable guidelines.

## Skills

| Skill | Purpose | Status |
| --- | --- | --- |
| [spec-authoring · Guideline Authoring](spec-authoring/SKILL.en.md) | Build or revise guidelines, forming shared principles, conventions, and boundaries from context and requirements while preserving choice of methods | Released `v0.2.2` |
| [spec-review · Review](spec-review/SKILL.en.md) | Review existing material against applicable guidelines, checking every applicable requirement and location and reporting findings in chat; the material may itself be a guideline document | Released `v0.2.2` |

Guideline Authoring applies wherever shared conventions are needed and does not prescribe fixed sections, steps, or output templates. Review is complete when all applicable requirements have been checked; methods and the organization of results suit the task, with delivery in chat by default.

## Language

Chinese is the primary version for maintenance and validation. English translations help readers understand the instructions and are kept aligned with their respective Chinese originals. If their meanings differ, the Chinese originals take precedence. See the translations of [Guideline Authoring](spec-authoring/SKILL.en.md) and [Review](spec-review/SKILL.en.md).

The installed entry point remains the Chinese `SKILL.md`, and the interface text remains in Chinese. You can specify the language of a task and its output. Providing an English translation does not mean that the effectiveness of English instructions has been validated.

## Installation

### Install with Codex

The two skills can be installed independently as needed.

To install Guideline Authoring, send this to Codex:

```text
$skill-installer install https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.2/spec-authoring
```

To install Review:

```text
$skill-installer install https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.2/spec-review
```

These URLs are pinned to `v0.2.2`. To follow the latest source, replace `v0.2.2` with `main`.

### Manual installation

Download the archive for the skill you need from [GitHub Releases](https://github.com/Ethan-decoy/spec-authoring-skill/releases), extract it, and place the entire `spec-authoring` or `spec-review` folder in the skill directory used by your Agent Skills-compatible tool.

For Codex, use `~/.agents/skills/` for your user account, or `.agents/skills/` in the target project. Keep each skill in its own folder named after the skill, containing `SKILL.md`. If the interface does not update, restart the client. See the [official Codex skill documentation](https://learn.chatgpt.com/docs/build-skills). For other tools, consult their documentation for discovery and installation.

## Usage

To build or revise guidelines:

```text
Use $spec-authoring to build or revise the guidelines we need, based on the current purpose, context, and available material.
```

Provide the material you have and the problem you need to resolve. You do not need to fill out a fixed set of fields in advance.

To review existing material against applicable guidelines:

```text
Use $spec-review to review the current material thoroughly against applicable guidelines and explain the findings, evidence, and review limitations in chat.
```

### Automatic invocation

The skills are distinguished by the requested action. Building or rewriting guidelines fits `spec-authoring`; reviewing existing material against guidelines to identify issues fits `spec-review`. For example, assessing whether a guideline document is reasonable is a review task, while revising it based on findings is an authoring task.

Both capabilities may contribute to one task as needed for the user's goal. Their own entry points express this division; extra global routing rules, skill names, or repeated copies of known guidelines are not prerequisites. Merely following existing conventions to perform an ordinary task does not by itself activate either skill.

Both skills allow automatic invocation. Selection matches the task to the skill description and is not guaranteed on every request. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills).

If you manually added the global routing example from `v0.2.1`, remove its old object-based routing paragraphs while preserving other existing guidance.

## Contents and principles

Read the [Chinese original](spec-authoring/SKILL.md) or the [English translation](spec-authoring/SKILL.en.md). The skill distinguishes confirmed requirements, observed practices, facts, and suggestions, preserving their conditions of applicability and unresolved issues. A practice does not become binding simply because it exists. The guidelines contain usable conventions; research and revision records are kept separately according to their purpose.

Review checks the source, applicable conditions, actual locations, and judgment for each requirement. Requirements that apply in several places are checked at every applicable location. It distinguishes evidence-supported compliance, deviations, non-applicability, insufficient evidence, and unchecked work. Results are delivered directly in chat without a separate coverage record or review document. Files for review material or revisions to the work are written only when the user explicitly requests those outputs or changes. Unresolved applicable requirements keep the review incomplete or its conclusion limited.

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

`v0.2.2` makes guideline construction and review against guidelines the two explicit entry points, updates the English translations and interface labels, and removes the previous recommendation to route by the type of object. Chinese is the primary maintenance version. Validation of `spec-authoring` includes format checks and a small number of drafting checks using real material.

One static comparison of `spec-review` has been completed using a local controlled variant of real guidelines and note material, checking requirement coverage, repeated applicable locations, and the handling of unverified properties. The change to delivery in chat by default was checked in a separate focused trial; workspace file contents were identical before and after that review. Neither skill has demonstrated consistent improvement across tasks and models.

Previous invocation trials had extra global routing enabled and cannot establish the skills' independent selection behavior. After removing that routing, this round used requests without skill names to check content review, guideline construction, review of a guideline document, and revision after review. Each used the corresponding skill. These remain limited agent trials, not evidence of invocation success rates across all clients or sessions.

Use [Issues](https://github.com/Ethan-decoy/spec-authoring-skill/issues) to share your intended use, the behavior you observed, and judgments that need improvement. Remove private information before sharing material.

## Maintenance

See [AGENTS.md](AGENTS.md) for the project maintenance instructions, which are in Chinese. Private samples, research drafts, individual validation outputs, and local release preparation files stay in the Git-ignored `local_artifacts/` directory. They are excluded from the public source and installation archive. Reusable examples require permission before they are added to the distributed resources.

## License

[MIT](LICENSE).
