---
title: please squash
weight: 13
---

Combines a run of commits into one, AI-written message and all.

<!--more-->

```bash
please squash
please squash 3
please squash main
```

The other boring, error-prone task nobody enjoys: `git rebase -i`, editing a todo file by hand, resolving whatever it trips on. please squash does it with a single `git reset --soft` back to a starting point instead, so there is no rebase to go wrong.

## Choosing what to squash

No argument squashes everything ahead of the branch's upstream, or the repository's default branch if it has not been pushed yet, the usual "clean up before merging" case.

A number squashes the last `<n>` commits.

A branch or commit name squashes back to it directly. It has to actually be an ancestor of HEAD, so this cannot jump the branch somewhere unrelated.

## Confirmation and pushing

Either way, please shows every commit about to be combined and requires typing yes first.

{{< callout type="warning" >}}
  If the branch has already been pushed, that same yes also covers force-pushing the result back with `--force-with-lease`, right after. It fails safely instead of clobbering anything if someone else pushed to the branch meanwhile.
{{< /callout >}}
