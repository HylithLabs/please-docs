---
title: please sync
weight: 5
---

Keeps your local branch aligned with its remote.

<!--more-->

## please sync

```bash
please sync
```

Fetches and merges the current branch's upstream in, like `git pull`. Reports up to date, or the merge result. On a real conflict, shows git's conflict output and points you to please commit once you have resolved it.

## please sync exactly

```bash
please sync exactly
```

Makes the local branch match its remote exactly. Discards local commits and uncommitted changes that are not on the remote. Untracked files are left alone.

{{< callout type="warning" >}}
  This is destructive. please shows exactly what will be lost and requires typing yes to proceed.
{{< /callout >}}
