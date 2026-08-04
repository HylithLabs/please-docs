---
title: Installation
weight: 1
---

Install please with a script, a package manager, or a direct download. All three install a prebuilt binary, no Rust toolchain required.

<!--more-->

## macOS and Linux

```bash
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/HylithLabs/please/releases/latest/download/please-installer.sh | sh
```

Detects your platform and installs the right binary, no separate download step.

## Windows

```powershell
powershell -ExecutionPolicy Bypass -c "irm https://github.com/HylithLabs/please/releases/latest/download/please-installer.ps1 | iex"
```

Or download the `.msi` below for a double-click installer instead of a script.

{{< callout type="warning" >}}
  The `.exe` and `.msi` are not code signed yet, so Windows SmartScreen may show **"Windows protected your PC."** This is a reputation check on unsigned software, not a virus detection. Click **More info**, then **Run anyway** to continue.
{{< /callout >}}

## Homebrew

```bash
brew install HylithLabs/please/please
```

## Download directly

Every release publishes prebuilt binaries for each platform. These links always point at the latest release.

{{< cards >}}
  {{< card link="https://github.com/HylithLabs/please/releases/latest/download/please-x86_64-pc-windows-msvc.msi" title="Windows Installer (.msi)" subtitle="x86_64, double-click to install" icon="device-desktop" />}}
  {{< card link="https://github.com/HylithLabs/please/releases/latest/download/please-x86_64-pc-windows-msvc.zip" title="Windows (.zip)" subtitle="x86_64, raw binary" icon="device-desktop" />}}
  {{< card link="https://github.com/HylithLabs/please/releases/latest/download/please-aarch64-apple-darwin.tar.xz" title="macOS (Apple Silicon)" subtitle="arm64" icon="device-desktop" />}}
  {{< card link="https://github.com/HylithLabs/please/releases/latest/download/please-x86_64-apple-darwin.tar.xz" title="macOS (Intel)" subtitle="x86_64" icon="device-desktop" />}}
  {{< card link="https://github.com/HylithLabs/please/releases/latest/download/please-x86_64-unknown-linux-gnu.tar.xz" title="Linux (x86_64)" subtitle="glibc" icon="device-desktop" />}}
  {{< card link="https://github.com/HylithLabs/please/releases/latest/download/please-aarch64-unknown-linux-gnu.tar.xz" title="Linux (arm64)" subtitle="glibc" icon="device-desktop" />}}
{{< /cards >}}

After extracting a `.tar.xz` or `.zip`, put the `please` binary somewhere on your `PATH` yourself — the shell/PowerShell installers and the `.msi` do that step for you, a raw download does not.

All release assets, including checksums, are on the [GitHub Releases page](https://github.com/HylithLabs/please/releases/latest).

## Build from source

Only needed if you'd rather not run a prebuilt binary. Requires a working Rust toolchain (cargo).

```bash
git clone https://github.com/HylithLabs/please.git
cd please
cargo install --path .
```

{{< callout type="info" >}}
  `please update` (see the [command reference](../../commands/update)) only works on the shell/PowerShell/`.msi` installs above — it has no source tree to rebuild a `cargo install` from, and a Homebrew install is updated with `brew upgrade please` instead.
{{< /callout >}}

## Verify

```bash
please help
```

Prints the full command reference grouped by what you are trying to do. If it prints, install succeeded.

## Next step

Run setup once per machine to connect an AI provider.

{{< cards >}}
  {{< card link="setup" title="Setup" subtitle="Connect please to Anthropic, Google, or OpenAI" icon="settings" />}}
{{< /cards >}}
