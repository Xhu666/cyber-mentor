# Cyber Mentor

[English](README.md) | [简体中文](README.zh-CN.md)

A Codex skill for reviewing and polishing academic papers and research project reports in two passes. It produces a complete revised manuscript as a separate file and preserves the original.

## Background

I am a PhD student in engineering at Tsinghua University. The Paper Writing Prompt grew out of frequent revisions of papers and research project reports with my advisor. I distilled the writing requirements and revision practices from that process into this prompt, then packaged it as Cyber Mentor to apply them consistently during document review.

## Workflow

1. **Paragraph review:** Apply the full [Paper Writing Prompt](references/paper-writing.md) to every paragraph, revising reasoning, sentence connections, clarity, and language. Use the bundled [Humanizer](references/humanizer/SKILL.md) to address formulaic writing while preserving research accuracy.
2. **Whole-document review:** Check relationships between paragraphs and sections, argument progression, consistency, repetition, and transitions.
3. **Delivery:** Save a complete revised manuscript in a new file, using the original format where possible. Finish both passes before delivering the result.

The skill preserves scientific meaning, data, equations, citations, technical boundaries, and existing unrelated edits. An explicit request to review only a particular section limits the scope accordingly.

## Installation

### Option 1: install with Git

Run these commands in a macOS or Linux terminal with Git installed:

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/Xhu666/cyber-mentor.git "$HOME/.agents/skills/cyber-mentor"
```

This installs the skill for your user account. To install it only for one project, run the following from that project's root instead:

```bash
mkdir -p .agents/skills
git clone https://github.com/Xhu666/cyber-mentor.git .agents/skills/cyber-mentor
```

Choose one installation location. If the target directory already exists, do not overwrite it. To update an existing Git installation, run `git -C "$HOME/.agents/skills/cyber-mentor" pull --ff-only` (adjust the path for a project installation).

### Option 2: ask Codex to install it

Paste this prompt into Codex:

```text
Install the Cyber Mentor skill from https://github.com/Xhu666/cyber-mentor
into ~/.agents/skills/cyber-mentor. Preserve the repository directory structure,
including the bundled Humanizer and its license. If that directory already
exists, inspect it first and do not overwrite local changes. Verify that
SKILL.md and its relative references are present, then explain how to invoke
$cyber-mentor.
```

Codex detects skill changes automatically. If the skill does not appear, restart Codex. You can then invoke `$cyber-mentor` as shown below. Installation locations follow the [official Codex skills documentation](https://developers.openai.com/codex/skills/).

## Usage

Invoke the skill in Codex and provide the manuscript path:

```text
Use $cyber-mentor to review /path/to/manuscript.tex. Complete both review
passes and save a separate revised manuscript without changing the original.
```

Research project reports are also supported:

```text
Use $cyber-mentor to review /path/to/research-report.docx. Preserve the report's
structure and scientific content, and deliver a complete revised copy.
```

The instructions are in English; the manuscript's language is preserved. Reading, editing, compiling, or rendering particular document formats requires suitable tools in your Codex environment. No separate Humanizer installation is required.

## Contents

```text
SKILL.md
agents/openai.yaml
references/paper-writing.md
references/humanizer/SKILL.md
references/humanizer/LICENSE
```

## Attribution

The bundled English Humanizer is version 3.0.0 of [blader/humanizer](https://github.com/blader/humanizer), copyright 2025 Siqi Chen, distributed under the [MIT License](references/humanizer/LICENSE). Its guidance draws on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).
