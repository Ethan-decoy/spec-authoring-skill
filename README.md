# spec-authoring-skill · 规范构建与审阅

[中文](README.md) · [English](README.en.md)

Agent Skills for authoring guidelines and reviewing work against them. Chinese is the primary version; English translations are available.

帮助 AI 构建规范，并依据适用规范审阅已有内容。

> 当前为实验分支 `codex/experimental-spec-guidance`，基于稳定版 `v0.2.2`。本次补充共同适用约定的取舍指导，以及审阅时证据应回答条款实际要求的指导，供实际使用测试。

## 技能

| 技能 | 用途 | 状态 |
| --- | --- | --- |
| [spec-authoring · 规范构建](spec-authoring/SKILL.md) | 构建或修订规范，将背景与要求形成共同原则、约定和边界，保留具体做法的选择空间 | 实验分支；稳定版为 `v0.2.2` |
| [spec-review · 审阅](spec-review/SKILL.md) | 依据适用规范审阅已有内容，核对全部适用要求和位置，在聊天中给出问题与判断；对象也可以是规范本身 | 实验分支；稳定版为 `v0.2.2` |

规范构建不以领域清单限定用途，也不要求固定栏目、执行步骤或输出模板。审阅以全部适用要求得到核对为完成标准，核对方式和结果组织按任务选择，默认在聊天中交付。

## 语言

中文是主要维护与验证的版本。英文译文供读者理解和参考，按各自的中文原文同步；含义出现差异时，以中文原文为准。参见[规范构建英文译文](spec-authoring/SKILL.en.md)与[审阅英文译文](spec-review/SKILL.en.md)。

安装后仍以中文 `SKILL.md` 为入口，界面说明保持中文。任务和输出语言可以按需要指定；提供英文译文不代表已经验证英文指令的使用效果。

## 安装

### 安装实验分支

将以下请求发送给 Codex，按需安装一个或两个技能。已安装同名技能时，以下请求明确要求替换为实验分支版本：

```text
$skill-installer 从 GitHub 仓库 Ethan-decoy/spec-authoring-skill 的 codex/experimental-spec-guidance 分支安装 spec-authoring，替换已有同名技能。
```

```text
$skill-installer 从 GitHub 仓库 Ethan-decoy/spec-authoring-skill 的 codex/experimental-spec-guidance 分支安装 spec-review，替换已有同名技能。
```

也可以[下载实验分支源码包](https://github.com/Ethan-decoy/spec-authoring-skill/archive/refs/heads/codex/experimental-spec-guidance.zip)，解压后按下文的手动安装方式使用对应技能文件夹。分支可能继续更新，反馈时请附上所测试的提交号。恢复稳定版时，使用下方固定到 `v0.2.2` 的入口并要求替换同名技能。

### 在 Codex 中安装稳定版

两个技能可以按需独立安装。

安装规范构建技能，向 Codex 发送：

```text
$skill-installer 安装 https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.2/spec-authoring
```

安装审阅技能：

```text
$skill-installer 安装 https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.2.2/spec-review
```

这些入口固定到 `v0.2.2`。需要跟随最新源码时，将链接中的 `v0.2.2` 换成 `main`。

### 手动安装

从 [GitHub Releases](https://github.com/Ethan-decoy/spec-authoring-skill/releases) 下载所需技能的压缩包，解压后将整个 `spec-authoring` 或 `spec-review` 文件夹放入支持 Agent Skills 的工具所使用的技能目录。

Codex 可使用用户目录 `~/.agents/skills/`，或目标项目中的 `.agents/skills/`。每个技能保留独立的同名目录，目录内应能找到 `SKILL.md`；若界面没有更新，可重启客户端。参见 [Codex 官方技能说明](https://learn.chatgpt.com/docs/build-skills)。其他工具的发现与安装方式以其文档为准。

## 使用

构建或修订规范：

```text
使用 $spec-authoring，根据当前目的、背景和已有材料，构建或修订所需规范。
```

提供手头已有的材料和需要解决的问题即可；不需要预先填满一套固定字段。

依据适用规范审阅已有内容：

```text
使用 $spec-review，依据适用规范完整审阅当前对象，在聊天中说明问题、依据和审阅限制。
```

### 自动调用

两个技能按动作分工。要形成或改写规范，适用于 `spec-authoring`；要审阅已有内容、依据规范给出问题与判断，适用于 `spec-review`。例如，“审阅这份规范是否合理”属于审阅，“根据意见修订这份规范”属于构建。

两项能力可以在一个任务中配合使用，具体安排服从用户目标。技能入口本身承载这层分工，不以额外的全局分派规则为使用前提，也不要求点名技能或重复提供已有规范。仅按既有约定执行普通任务时，不因此额外调用。

两个技能都允许自动调用。自动选择由模型结合任务与技能描述完成，不能保证每次都选中；参见 [Codex 技能说明](https://learn.chatgpt.com/docs/build-skills#how-chatgpt-and-codex-use-skills)。

如果此前手动加入了 `v0.2.1` 的全局分工示例，应移除其中按对象类型分派的旧段落，保留其他既有指引。

## 内容与原则

技能正文见[中文原文](spec-authoring/SKILL.md)与[英文译文](spec-authoring/SKILL.en.md)。它区分已确认的要求、观察到的做法、事实与建议，保留适用条件和未决事项；既有做法不会仅因存在就自动取得约束效力。规范正文承载可使用的约定，研究和修改过程按用途另行安置。

审阅逐项核对条款来源、适用条件、实际检查位置及结论。适用于多处的要求检查所有适用位置，区分有证据支持的符合、偏离、不适用、证据不足与未检查。结果直接在聊天中给出，无需另交覆盖记录或审阅文档；只有用户明确要求保存材料或修订产物时才写入相应文件。适用要求未核实时，结论保持未完成或受限。

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

当前实验改动已完成技能格式检查、中英文对应检查和本地分析模板复析。模板复析评估的是指令设计，不能证明实际使用效果。小范围静态对照试用尚未观察到明确优势，跨任务、跨模型的稳定改善仍待验证。

`v0.2.2` 将两个技能的入口明确为“构建规范”和“依据规范审阅”，同步中英文说明及界面名称，并移除此前以对象类型划分职责的全局路由建议。中文为主要维护版本，英文为对应译文。`spec-authoring` 已进行格式校验和少量实际材料的起草检查。

`spec-review` 已用实际规范与笔记的本地受控副本完成一次静态对照试用，检查条款覆盖、重复适用位置及未验证项的处理。默认聊天交付的调整另经小范围试用，试用前后工作区文件状态一致。两项技能都尚未证明跨任务、跨模型的稳定改善。

此前的触发试用启用了额外全局路由，不能用于证明技能自身的自动选择表现。本轮撤掉该路由后，以不点名技能的请求检查内容审阅、规范构建、规范自身的审阅及审阅后的修订，分别使用了对应技能。这些仍是小范围代理试用，不代表所有客户端或会话中的实际自动调用成功率。

欢迎通过 [Issues](https://github.com/Ethan-decoy/spec-authoring-skill/issues) 反馈预期用途、实际表现及需要改进的判断。分享材料前请移除私人信息。

## 维护

维护入口见 [AGENTS.md](AGENTS.md)。私人样例、研究草稿、单次验证产物和本地发布准备文件放在 Git 忽略的 `local_artifacts/`，不进入公开源码或安装包。可复用示例须获得保留许可后再纳入正式资源。

## 许可

[MIT](LICENSE)。
