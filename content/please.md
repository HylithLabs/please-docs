---
title: "PLEASE CLI"
description: "PLEASE is an AI-native Git command line tool that lets you interact with Git using plain language, automated commit splitting, and safe agent execution."
lead: "Talk to Git in plain language. AI-assisted commits, plain-language status, and intelligent agent mode built directly into your terminal."
date: 2026-08-05T00:00:00+00:00
url: "/please/"
---

**PLEASE** is a command-line interface designed to eliminate Git friction. You never type complex raw Git commands or struggle with commit messages again. Run `please` commands instead, and an AI agent handles staging, commit message generation, and branch operations on your behalf.

---

### Key Features

#### 🤖 AI-Powered Commits
Run `please commit` to inspect modified files, split changes into logical units, and generate clean, standardized commit messages automatically.

#### 💬 Agent Mode
Run `please` followed by any plain-language request in quotes (e.g., `please "sync with main and resolve conflicts"`). The AI agent formulates an execution plan and safely executes commands through Git and GH CLI.

#### 🛡️ Built-in Safety Nets
Destructive operations (force push, hard reset, branch deletion) require explicit confirmation up front. Sensitive environment files (`.env`, secrets) are protected from accidental commits.

#### 🔌 Choice of AI Provider
Connect to your preferred AI model—**Anthropic Claude**, **Google Gemini**, or **OpenAI ChatGPT**. Switch providers anytime without losing saved keys.

---

### Command Quick Reference

| Command | Action |
| :--- | :--- |
| **`please commit`** | Analyze diffs, stage files, and generate commit messages |
| **`please push`** | Commit staged work and push the current branch to origin |
| **`please status`** | View branch status and changes explained in plain language |
| **`please branch`** | Create, switch, rename, or clean up branches |
| **`please sync`** | Rebase or merge current branch with main safely |
| **`please undo`** | Revert recent commits or restore previous working state |
| **`please squash`** | Combine a run of commits into one, AI-written message |
| **`please update`** | Update please itself to the latest release |

---

### Getting Started

1. **Install PLEASE:**
   See the [Installation Guide](/docs/getting-started/installation/) to install a prebuilt binary with a script, Homebrew, or a direct download, or build it from source.

2. **Connect your Provider:**
   Run `please setup` to configure your API key.

3. **Read Documentation:**
   Explore the full [Command Reference](/docs/commands/please-commit/) to master PLEASE.
