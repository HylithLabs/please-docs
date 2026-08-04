---
title: Roadmap
weight: 4
prev: /docs/concepts/design-philosophy
---

Where please is headed, drawn from the project vision document.

<!--more-->

## Vision

please aims to become a full AI native git distribution, in the same spirit as Microsoft's git distribution with Scalar: extending git while preserving its core functionality. The goal is not to replace git, but to build an AI powered layer on top of it that developers reach for instead of raw git commands.

## Planned: a native distribution

Today please installs as a cargo package on top of an existing git install. The longer term plan is an installer per operating system, a Windows executable, a Linux package, a macOS package, so a user installs please and gets a full git distribution with the AI layer already built in.

## Planned: a configuration GUI

A graphical interface for managing provider, API key, model selection, and other software settings, as an alternative to running please setup from the terminal. Once configured, development continues primarily from the terminal, the same as today.

## Planned: Auto Commit

A future capability where please continuously monitors changes in the codebase. When it determines you have completed a meaningful unit of work, it automatically creates a commit for those changes without you running a commit command yourself. The AI manages commit creation as development progresses, rather than waiting for you to run please commit.

{{< callout type="info" >}}
  Auto Commit and the configuration GUI are both forward looking. Check the project source for current implementation status before relying on either.
{{< /callout >}}
