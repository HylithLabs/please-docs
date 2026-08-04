---
title: please undo and please redo
weight: 6
---

Take back a commit, or bring it back.

<!--more-->

## please undo

```bash
please undo
```

Undoes the last commit, replacing `git reset --soft HEAD~1`. The changes land back in your working tree so you can fix them and try again.

## please redo

```bash
please redo
```

Brings back what please undo removed, as long as history has not moved on since. A new commit invalidates it.
