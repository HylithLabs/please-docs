---
title: please commit
weight: 1
url: /docs/commands/please-commit/
aliases:
  - /docs/commands/commit/
prev: /docs/getting-started/setup
next: /docs/commands/push
---

Stages your changes, sends the diff to the AI, and lets it split the work into one or more logically coherent commits, each with its own files and message.

<!--more-->

```bash
please commit
```

You never run git add or write a commit message yourself.

## Guardrails

Two checks run automatically before staging.

Sensitive files, `.env`, credentials, private keys, and similar, are skipped unless you already staged them yourself. Staging a sensitive file yourself is treated as explicit intent to include it.

Build and dependency directories, `node_modules`, `dist`, `target`, `.venv`, and similar, that are not already tracked or ignored get added to `.gitignore` automatically. This keeps beginners without a `.gitignore` from accidentally committing junk.

{{< callout type="info" >}}
  Want a sensitive file included anyway? Stage it yourself with git add first, then run please commit. please treats that as your explicit choice.
{{< /callout >}}
