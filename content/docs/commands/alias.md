---
title: please alias
weight: 12
---

Give please a shorter name, like pls or plz, so casual daily use is less to type.

<!--more-->

## Create an alias

```bash
please alias pls
```

This creates a real symlink next to the please binary itself, so pls becomes a genuine command. It works in every shell and in scripts, and it does not need a new terminal or a sourced rc file to take effect.

## List aliases

```bash
please alias
```

Lists what you have set up.

## Remove an alias

```bash
please alias remove pls
```

Takes one back.

## Name collisions

If the name you pick already exists as a different program elsewhere on your PATH, please warns before shadowing it and asks you to confirm. If it collides with an unrelated file right next to please itself, please refuses outright rather than overwriting something that is not its own.
