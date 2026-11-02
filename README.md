> [!NOTE]
> **This skill lives in the main collection: [milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills/tree/main/skills/skill-finder)**. Please ⭐ star it there; that's where updates land first.
> Docs: **https://milad-ahmd.github.io/agent-skills/skills/skill-finder/** · Claude Code: `/plugin install all-skills --marketplace milad-ahmd/agent-skills`

<div align="center">

# 🧭 skill-finder

**Describe a task, get the right existing skill with why it fits, and install it only on your OK. An Agent Skill for Claude Code, Cline, Cursor, Codex and other AI coding agents.**

[![License: MIT](https://img.shields.io/github/license/milad-ahmd/skill-finder)](LICENSE)
[![Stars](https://img.shields.io/github/stars/milad-ahmd/skill-finder?style=social)](https://github.com/milad-ahmd/skill-finder)
![Category](https://img.shields.io/badge/category-Agent%20Productivity-blue)
![Works with](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Cline%20%7C%20Cursor%20%7C%20Codex-8A2BE2)

[Install](#-install) · [Usage](#-usage) · [How it works](skills/skill-finder/SKILL.md) · [All skills](https://github.com/milad-ahmd/agent-skills)

</div>

> Part of **[agent-skills](https://github.com/milad-ahmd/agent-skills)**, a growing collection of practical skills for AI coding agents.

## 📦 Install

**One command (installs the whole collection):**

```bash
curl -fsSL https://raw.githubusercontent.com/milad-ahmd/agent-skills/main/install.sh | bash -s -- skill-finder
```

**Manually (Claude Code):**

```bash
git clone https://github.com/milad-ahmd/skill-finder /tmp/skill-finder
mkdir -p ~/.claude/skills && cp -r /tmp/skill-finder/skills/skill-finder ~/.claude/skills/
```

**Per project:** copy `skills/skill-finder` into `<project>/.claude/skills/`.
**Any other agent:** paste [`SKILL.md`](skills/skill-finder/SKILL.md) into your rules or system prompt.

## 💬 Usage

Just ask your agent:

```text
Is there a skill for turning meeting notes into Jira tickets?
Find me a skill for Playwright tests and install it
```

The full workflow, rules and output format are in [`SKILL.md`](skills/skill-finder/SKILL.md).

## 🔎 Sample output

`find_skill.py` is plain Python 3 with no dependencies and searches an index of this collection. Real output:

```text
$ python3 find_skill.py "my docker image is 2GB and builds take forever" --top 2

Skills for "my docker image is 2GB and builds take forever":

1. dockerize-anything  (score 14.59; matched: docker, imag, build)
   Production-ready, small, secure Dockerfile and compose for any repo
   install:  curl -fsSL -o /tmp/agent-skills-install.sh https://raw.githubusercontent.com/milad-ahmd/agent-skills/main/install.sh && bash /tmp/agent-skills-install.sh dockerize-anything
   or:       npx skills add milad-ahmd/agent-skills --skill dockerize-anything

2. screenshot-to-component  (score 6.51; matched: imag, build)
   Screenshot or mockup to a component built with your design system
   install:  curl -fsSL -o /tmp/agent-skills-install.sh https://raw.githubusercontent.com/milad-ahmd/agent-skills/main/install.sh && bash /tmp/agent-skills-install.sh screenshot-to-component
   or:       npx skills add milad-ahmd/agent-skills --skill screenshot-to-component

Claude Code, whole collection: /plugin install all-skills --marketplace milad-ahmd/agent-skills
```

When nothing here fits, it exits 1 and suggests `npx skills find <keywords>` to search the wider skills.sh registry. The agent installs only after you say yes.

## 🧩 More skills

See the full collection: **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 🤝 Contributing

This repo is a read-only mirror. Please open issues and PRs in **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 📄 License

[MIT](LICENSE) © Milad Ahmadi

<div align="center">

**If this skill saved you time, a ⭐ helps others find it.**

</div>
