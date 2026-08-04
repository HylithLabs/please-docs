---
linkTitle: "Documentation"
title: Introduction
---

Welcome to the please documentation.

<!--more-->

## What is please

please is an AI native git command line tool. You never type raw git commands. You run please commands instead, and an AI agent, your choice of Anthropic Claude, Google Gemini, or OpenAI ChatGPT, handles staging, commit messages, and pushing on your behalf.

Git remains the engine underneath. please is the interface.

Run please with no arguments, or please help, any time for a full command reference grouped by what you are trying to do.

## Design principles

{{< cards >}}
  {{< card link="../concepts/design-philosophy" title="No hand written git" subtitle="Every git operation a developer needs is reachable through a please command" icon="terminal" />}}
  {{< card link="../concepts/safety-nets" title="Confirmation before damage" subtitle="Anything that can discard work explains the consequences and asks first" icon="shield-check" />}}
  {{< card link="../concepts/providers" title="Your choice of provider" subtitle="Anthropic, Google, or OpenAI, switch any time without losing saved keys" icon="adjustments" />}}
{{< /cards >}}

## Next

{{< cards >}}
  {{< card link="getting-started/installation" title="Getting Started" subtitle="Install please and run setup" icon="file-text" />}}
  {{< card link="commands" title="Commands" subtitle="Full command reference" icon="stack" />}}
{{< /cards >}}
