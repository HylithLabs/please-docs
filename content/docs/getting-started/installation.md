---
title: Installation
weight: 1
---

please is built in Rust. Install it with cargo from the project source.

<!--more-->

## Requirements

You need a working Rust toolchain (cargo) and git already installed on your machine.

## Install with cargo

From the root of the please project source:

```bash
cargo install --path .
```

This builds the binary and places it on your PATH so the please command is available from any directory.

## Verify

```bash
please help
```

This prints the full command reference grouped by what you are trying to do. If it prints, install succeeded.

## Next step

Run setup once per machine to connect an AI provider.

{{< cards >}}
  {{< card link="setup" title="Setup" subtitle="Connect please to Anthropic, Google, or OpenAI" icon="cog" />}}
{{< /cards >}}
