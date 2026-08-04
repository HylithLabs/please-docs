---
title: History Fixes
weight: 7
---

Three commands for fixing mistakes already in your commit history.

<!--more-->

## please move-commit

```bash
please move-commit <branch>
```

Fixes committing to the wrong branch: moves your last commit onto a new branch and switches you to it. Replaces `git branch new`, `git reset --hard HEAD~1`, and `git checkout new`.

Refuses if you have uncommitted changes, so nothing else gets swept up in the move.

## please restore

```bash
please restore <path>
```

Brings back a file that was deleted in a past commit. Replaces hunting through `git log --diff-filter=D` for the deleting commit and running `git checkout <sha>^ -- <path>` yourself.

## please revert

```bash
please revert
```

Interactive, no AI involved. Lists your recent commits with a serial number and hash next to each. You pick one either way, and it is reverted. Replaces hunting down a SHA with git log and running `git revert <sha>` yourself.

If your working tree is dirty, please tells you up front to run please commit or please discard first, rather than running into a wall of uncommitted changes. If the revert itself conflicts, it lists the conflicting files and tells you to resolve them and run please commit, or please discard to cancel.
