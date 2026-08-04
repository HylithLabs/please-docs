---
title: Branches
weight: 4
---

Commands for creating, switching, renaming, and cleaning up branches.

<!--more-->

## please branch

```bash
please branch
please branch <name>
```

With no name, lists local branches. With a name, creates and switches to a new branch.

## please switch

```bash
please switch <name>
```

Switches to an existing branch. If the branch does not exist, please offers to create and switch to it.

## please rename

```bash
please rename <new-name>
```

Renames the current branch, including on the remote if it has already been pushed. Replaces running `git branch -m old new`, `git push origin -u new`, and `git push origin --delete old` yourself.

## please cleanup

```bash
please cleanup
```

Deletes local branches already merged into the repository's main branch. Replaces `git branch --merged main | grep -v main | xargs git branch -d`.

Only ever removes branches git already considers safe to delete, the same guarantee as `git branch -d`, never the forced `-D`.

## please branch delete

```bash
please branch delete <name>
```

Deletes a branch locally and on origin in one step. Replaces `git branch -d name` followed by `git push origin --delete name`.

{{< callout type="warning" >}}
  please branch delete refuses to delete the branch you are currently on.
{{< /callout >}}
