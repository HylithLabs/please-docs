---
title: please purge
weight: 14
---

Permanently removes a file or folder from your entire git history, not just the working tree.

<!--more-->

```bash
please purge secrets.env
please purge config/credentials
```

The boring, error-prone task of scrubbing a leaked secret or an accidentally committed file out of every commit that ever touched it.

## How it works

please uses `git filter-repo` if it is installed, git's own recommended tool for this, falling back to the built-in `git filter-branch` otherwise. It then cleans up the now-unreachable objects so the old content is actually gone, not just unreferenced.

## Confirmation and pushing

This rewrites commit hashes for the file's entire history and everything after it, so please shows you exactly what that means and requires typing yes first.

{{< callout type="warning" >}}
  If you have an origin remote, that same yes also force-pushes the rewritten history there right after, since a leaked secret is still live on the remote until that happens. You are told upfront that is part of the plan.
{{< /callout >}}

Every collaborator needs to re-clone or run `please sync exactly` afterward, since their local history has now diverged permanently.
