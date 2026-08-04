---
title: Design Philosophy
weight: 3
---

The principles please is built around.

<!--more-->

## No hand written git

Every git operation a developer needs is reachable through a please command. The goal is that you never need to drop down to raw git yourself.

## Explicit overrides, not blanket blocks

Guardrails, the sensitive file check and the junk directory check, can always be bypassed by staging the file yourself first. please assumes intent over blocking outright.

## Bounded AI latency

The model's own response time is not something please controls, but everything around it is. Requests are timeout bounded, progress is printed so the CLI never looks frozen, and the model is auto selected once at setup, self healing on failure, rather than re selected on every call.

## Destructive operations require confirmation

Anything that can discard work, such as please sync exactly, explains the consequences up front and requires explicit confirmation.

See [Safety Nets](../safety-nets) for the full picture, including the extra layer that applies inside agent mode.
