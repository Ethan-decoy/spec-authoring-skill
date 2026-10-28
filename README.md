# spec-authoring · 规范编写

[中文](README.md) · [English](README.en.md)

An Agent Skill for drafting, revising, and reviewing guidelines. It clarifies shared understanding, principles, and boundaries while leaving room for judgment. Chinese is the primary version; an English translation is available.

帮助 AI 根据实际目的、背景和已有材料编写、修订或评审规范。以适当约束形成共同理解和判断依据，在符合目的、原则和边界的前提下，尽量保留具体做法的选择空间。

技能不以领域清单限定用途，也不要求固定栏目、执行步骤或输出模板。仅依据既有规范完成其他任务时，无需使用本技能。

## 语言

中文是主要维护与验证的版本。[英文技能译文](spec-authoring/SKILL.en.md)供读者理解和参考，按中文原文同步；含义出现差异时，以[中文原文](spec-authoring/SKILL.md)为准。

安装后仍以中文 `SKILL.md` 为入口，界面说明保持中文。任务和输出语言可以按需要指定；提供英文译文不代表已经验证英文指令的使用效果。

## 安装

### 在 Codex 中安装

向 Codex 发送：

```text
$skill-installer 安装 https://github.com/Ethan-decoy/spec-authoring-skill/tree/v0.1.1/spec-authoring
```

该入口固定到 `v0.1.1`。需要跟随最新源码时，将链接中的 `v0.1.1` 换成 `main`。

### 手动安装

从 [GitHub Releases](https://github.com/Ethan-decoy/spec-authoring-skill/releases) 下载技能压缩包，解压后将整个 `spec-authoring` 文件夹放入支持 Agent Skills 的工具所使用的技能目录。

Codex 可使用用户目录 `~/.agents/skills/spec-authoring/`，或目标项目中的 `.agents/skills/spec-authoring/`。安装后应能找到 `SKILL.md`；若界面没有更新，可重启客户端。参见 [Codex 官方技能说明](https://learn.chatgpt.com/docs/build-skills)。其他工具的发现与安装方式以其文档为准。

## 使用

```text
使用 $spec-authoring，根据当前目的、背景和已有材料，起草或修订所需规范。
```

提供手头已有的材料和需要解决的问题即可；不需要预先填满一套固定字段。

## 内容与原则

技能正文见[中文原文](spec-authoring/SKILL.md)与[英文译文](spec-authoring/SKILL.en.md)。它区分已确认的要求、观察到的做法、事实与建议，保留适用条件和未决事项；既有做法不会仅因存在就自动取得约束效力。规范正文承载可使用的约定，研究和修改过程按用途另行安置。

```text
spec-authoring/
├── SKILL.md
├── SKILL.en.md
├── LICENSE
└── agents/
    └── openai.yaml
```

技能不包含可执行脚本或外部服务依赖。

## 试用与反馈

当前版本为 `v0.1.1` 公开试用版，在 `v0.1.0` 的基础上增加英文阅读材料，中文技能正文未变。已进行格式校验和少量实际材料的起草检查，尚未证明跨任务、跨模型的稳定改善。

欢迎通过 [Issues](https://github.com/Ethan-decoy/spec-authoring-skill/issues) 反馈预期用途、实际表现及需要改进的判断。分享材料前请移除私人信息。

## 维护

维护入口见 [AGENTS.md](AGENTS.md)。私人样例、研究草稿、单次验证产物和本地发布准备文件放在 Git 忽略的 `local_artifacts/`，不进入公开源码或安装包。可复用示例须获得保留许可后再纳入正式资源。

## 许可

[MIT](LICENSE)。
