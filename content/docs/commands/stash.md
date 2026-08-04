---
title: please stash
weight: 9
---

Save your working tree aside and come back to it later. No AI involved in any of these.

<!--more-->

## please stash

```bash
please stash
```

Saves everything in the working tree, tracked and untracked, and clears it, so you can switch context and come back later. Replaces `git stash push -u`.

## please stash list

```bash
please stash list
```

Shows what is saved.

## please stash pop

```bash
please stash pop
```

Restores the most recent stash. If it conflicts, please lists the conflicting files and tells you to resolve them and run please commit, or please discard to cancel the restore, which cleanly cancels it without losing the stash.

## please stash drop

```bash
please stash drop
```

Deletes the most recent stash outright.

{{< callout type="warning" >}}
  This is destructive. please shows what will be deleted and requires typing yes first, since a dropped stash cannot be recovered afterward.
{{< /callout >}}
