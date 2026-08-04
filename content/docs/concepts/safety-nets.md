---
title: Safety Nets
weight: 1
---

please can discard work. It never does so quietly.

<!--more-->

## Destructive operations require confirmation

Anything that can discard work, please sync exactly, please discard, please revert on a conflict cancel path, please stash drop, explains the consequences up front and requires you to type yes before it proceeds.

See the reference table on the [Commands](../../commands) page for which commands are marked destructive.

## Explicit overrides, not blanket blocks

Guardrails such as the sensitive file check and the junk directory check in please commit can always be bypassed by staging the file yourself first. please assumes intent over blocking outright: if you already ran git add on a `.env` file, that is treated as your explicit choice to include it.

## Two safety nets in agent mode

Agent mode and please chat add a second layer on top of the destructive operation confirmations.

Anything destructive run via raw git or gh, a force push, `reset --hard`, `branch -D`, deleting things, stops and asks you to confirm before running.

Any please subcommand that would normally ask for confirmation itself cannot be rubber stamped by the agent. It cancels itself exactly as it would for any non interactive caller, and the agent relays that back to you rather than pretending it succeeded.

See [Agent Mode](../../commands/agent-mode) for the full explanation.
