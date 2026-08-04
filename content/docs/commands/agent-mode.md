---
title: Agent Mode
weight: 10
---

Anything you type that is not one of the named commands is treated as a plain language request.

<!--more-->

```bash
please "clean up branches that are already merged into main"
please "what changed in the last 3 commits"
please "I broke something, undo my last commit"
please "open a PR for this branch"
```

The AI figures out how to do it and acts on your behalf. It never edits files directly. It only acts through git, gh, or another please subcommand, and it can call please itself recursively where that helps. For example, commit and clean up merged branches might run please commit, then please cleanup.

## Two safety nets

Anything destructive run via raw git or gh, a force push, `reset --hard`, `branch -D`, deleting things, stops and asks you to confirm before running.

Any please subcommand that would normally ask for confirmation itself, please discard, please sync exactly, please revert, please stash drop, or creating a branch via please switch, cannot be rubber stamped by the agent. It cancels itself exactly as it would for any non interactive caller, and the agent relays that back to you rather than pretending it succeeded. You run it yourself and confirm it directly.

## How providers plug in

The tool calling conversation is represented in provider neutral terms internally. Only a small adapter per provider, Gemini, Claude, ChatGPT, translates that to and from its own wire format. This is what lets please add new providers without touching the agent loop itself.
