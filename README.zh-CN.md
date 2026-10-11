# Cyber Mentor（赛博导师）

[English](README.md) | [简体中文](README.zh-CN.md)

用于论文和科研项目报告审核润色的 Codex skill。通过两遍审核生成完整的新版本稿件，保留原稿。

## 提示词的来源

我是清华大学的在读工科博士。这份论文写作提示词是在与导师频繁修改论文和科研项目报告的过程中逐步总结形成的。我将这一过程中积累的写作要求和修改经验整理成提示词，再封装为 Cyber Mentor，便于在稿件审核中持续应用。

## 工作流程

1. **逐段审核**：完整执行[论文写作提示词](references/paper-writing.md)，逐段检查和修改论证、句子衔接、内容清晰度及语言表达。使用内置的 [Humanizer](references/humanizer/SKILL.md) 检查模板化表达，同时保留科研准确性。
2. **全文审核**：检查段落和章节之间的关系、论证推进、前后一致性、重复内容及衔接。
3. **生成新稿**：完成两遍审核后，将完整修改稿保存为独立文件，尽可能沿用原稿格式，不直接修改原稿。

采用满足目标的最小改动，保留科学含义、数据、公式、引用、技术边界和用户已有的无关改动。用户明确限定某一节或问题时，仅完成指定范围。

## 安装

下载或克隆本仓库，将仓库内容放入 `~/.codex/skills/cyber-mentor/`。如果使用自定义 Codex 主目录，则放入 `$CODEX_HOME/skills/cyber-mentor/`。保留目录结构，以确保相对链接有效。

## 使用方法

在 Codex 中调用 skill，并提供稿件路径：

```text
使用 $cyber-mentor 审核 /path/to/manuscript.tex，完成两遍审核和润色，
生成完整的新版本稿件，不修改原稿。
```

也可以审核科研项目报告：

```text
使用 $cyber-mentor 审核 /path/to/research-report.docx，保留报告结构和科研内容，
完成逐段审核与全文逻辑检查后，生成完整的新版本报告。
```

skill 内部提示词采用英文，但会保留稿件原有语言。读取、编辑、编译或渲染特定文档格式，需要 Codex 环境中具备相应工具。无需单独安装 Humanizer。

## 文件结构

```text
SKILL.md
agents/openai.yaml
references/paper-writing.md
references/humanizer/SKILL.md
references/humanizer/LICENSE
```

## 来源与许可证

内置英文 Humanizer 来自 [blader/humanizer](https://github.com/blader/humanizer)，版本为 3.0.0，版权归 2025 Siqi Chen 所有，按 [MIT License](references/humanizer/LICENSE) 分发。其写作指南参考 Wikipedia 的 [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)。
