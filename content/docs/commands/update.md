---
title: please update
weight: 15
---

Updates please itself to the latest release, in place.

<!--more-->

```bash
please update
```

## Requirements

Only works if please was installed via the shell or PowerShell installer, or the `.msi`, see [Installation](../../getting-started/installation). Those leave behind a record of how they installed it that please update reads to find and replace the running binary.

{{< callout type="info" >}}
  Installed a different way? please update tells you what to do instead of failing mysteriously: `cargo install --path .` builds have no such record to read, rebuild from source instead. Homebrew installs are managed by brew, not please, run `brew upgrade please` instead.
{{< /callout >}}
