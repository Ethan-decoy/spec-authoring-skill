# spec-authoring-skill · 规范编写与审阅

[中文](README.md) · [English](README.en.md)

Agent Skills for authoring guidelines and reviewing work against them. Chinese is the primary version; English translations are available.

帮助 AI 建立适当的共同约定，并完整检查实际产物是否遵守这些约定。

## 技能

| 技能 | 用途 | 状态 |
| --- | --- | --- |
| [spec-authoring · 规范编写](spec-authoring/SKILL.md) | 编写、修订或评审规范本身，以适当约束明确目的、原则与边界，保留具体做法的选择空间 | 已发布 `v0.2.1` |
| [spec-review · 规范对照审阅](spec-review/SKILL.md) | 依据既有规范逐项检查产物，核对全部适用要求和位置，在聊天中交付结论 | 已发布 `v0.2.1` |

规范编写不以领域清单限定用途，也不要求固定栏目、执行步骤或输出模板。规范对照审阅以全部适用要求得到核对为完成标准，核对方式和结果组织按任务选择，默认在聊天中交付。

## 语言

中文是主要维护与验证的版本。英文译文供读者理解和参考，按各自的中文原文同步；含义出现差异时，以中文原文为准。参见[规范编写英文译文](spec-authoring/SKILL.en.md)与[规范对照审阅英文译文](spec-review/SKILL.en.md)。

安装后仍以中文 `SKILL.md` 为入口，界面说明保持中文。任务和输出语言可以按需要指定；提供英文译文不代表已经验证英文指令的使用效果。

## 安装

### 在 Codex 中安装

两个技能可以按需独立安装。

安装规范编写技能，向 Codex 发送：

```text
$skill-installer 安装 https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.1/spec-authoring
```

安装规范对照审阅技能：

```text
$skill-installer 安装 https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.1/spec-review
```

这些入口固定到 `v0.2.1`。需要跟随最新源码时，将链接中的 `v0.2.1` 换成 `main`。

### 手动安装

从 [GitHub Releases](https://github.com/Ethan-decoy/spec-authoring-skill/releases) 下载所需技能的压缩包，解压后将整个 `spec-authoring` 或 `spec-review` 文件夹放入支持 Agent Skills 的工具所使用的技能目录。

Codex 可使用用户目录 `~/.agents/skills/`，或目标项目中的 `.agents/skills/`。每个技能保留独立的同名目录，目录内应能找到 `SKILL.md`；若界面没有更新，可重启客户端。参见 [Codex 官方技能说明](https://learn.chatgpt.com/docs/build-skills)。其他工具的发现与安装方式以其文档为准。

## 使用

编写或评审约定本身：

```text
使用 $spec-authoring，根据当前目的、背景和已有材料，起草或修订所需规范。
```

提供手头已有的材料和需要解决的问题即可；不需要预先填满一套固定字段。

依据既有规范审阅产物：

```text
使用 $spec-review，依据适用规范完整审阅当前产物，在聊天中说明问题、依据和审阅限制。
```

### 自动调用

两个技能都允许自动调用。请求“按……规范审阅……”，或上下文已有对象和适用约定时说“审阅一下”“再检查一遍”，适用于 `spec-review`；希望形成共同约定、调整过度约束或评估规则本身时，适用于 `spec-authoring`。不要求点名技能或重复提供已有规范。

自动选择依据技能描述与任务的匹配，不能保证每次都选中。希望在已安装相应技能的环境中更明确地分派这类任务时，可在已使用的用户全局或项目 `AGENTS.md` 中按需追加简短指引：[Codex 技能说明](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills)。

```text
按规范或已有约定审阅、复核产物时，使用 $spec-review；上下文已明确对象与约定时，简短的“审阅一下”也按此处理。
编写、整理、修订或评估约定本身时，使用 $spec-authoring。仅按既有约定执行任务时，不因此调用这两项技能。
```

安装包本身不改写用户的全局指引。新增指引后，可用新会话验证，避免沿用启动时已加载的旧指引；参见 [AGENTS.md 的发现规则](https://learn.chatgpt.com/docs/agent-configuration/agents-md#how-codex-discovers-guidance)。

## 内容与原则

技能正文见[中文原文](spec-authoring/SKILL.md)与[英文译文](spec-authoring/SKILL.en.md)。它区分已确认的要求、观察到的做法、事实与建议，保留适用条件和未决事项；既有做法不会仅因存在就自动取得约束效力。规范正文承载可使用的约定，研究和修改过程按用途另行安置。

规范对照审阅逐项核对条款来源、适用条件、实际检查位置及结论。适用于多处的要求检查所有适用位置，区分有证据支持的符合、偏离、不适用、证据不足与未检查。结果直接在聊天中给出，无需另交覆盖记录或审阅文档；只有用户明确要求保存材料或修订产物时才写入相应文件。适用要求未核实时，结论保持未完成或受限。

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

技能不包含可执行脚本或外部服务依赖。

## 验证与反馈

`v0.2.1` 改进了两个技能的触发描述、自动调用配置及简短请求的处理，并提供可选的常驻分工指引。中文为主要维护版本，英文为对应译文。`spec-authoring` 已进行格式校验和少量实际材料的起草检查。

`spec-review` 已用实际规范与笔记的本地受控副本完成一次静态对照试用，检查条款覆盖、重复适用位置及未验证项的处理。默认聊天交付的调整另经小范围试用，试用前后工作区文件状态一致。两项技能都尚未证明跨任务、跨模型的稳定改善。

本次触发调整经过不点名技能的规范对照审阅、规则调整和普通文本替换试用，分别选择了对应技能或保持不调用。这是小范围代理试用，不代表所有客户端或会话中的实际自动调用成功率。

欢迎通过 [Issues](https://github.com/Ethan-decoy/spec-authoring-skill/issues) 反馈预期用途、实际表现及需要改进的判断。分享材料前请移除私人信息。

## 维护

维护入口见 [AGENTS.md](AGENTS.md)。私人样例、研究草稿、单次验证产物和本地发布准备文件放在 Git 忽略的 `local_artifacts/`，不进入公开源码或安装包。可复用示例须获得保留许可后再纳入正式资源。

## 许可

[MIT](LICENSE)。
