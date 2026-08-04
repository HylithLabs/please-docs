---
title: Commands
weight: 2
prev: /docs/getting-started/setup
next: /docs/commands/commit
sidebar:
  open: true
---

Full command reference, grouped by what you are trying to do.

<!--more-->

## Reference table

| Command | What it does | Destructive |
| --- | --- | --- |
| `please commit` | Stages changes and writes commits with the AI | No |
| `please push` | Runs commit, then pushes to origin | No |
| `please status` | Plain language view of where you stand | No |
| `please branch [name]` | Lists branches, or creates and switches to one | No |
| `please switch <name>` | Switches to an existing branch | No |
| `please sync` | Fetches and merges the upstream branch | No |
| `please sync exactly` | Makes the local branch match the remote exactly | Yes |
| `please undo` | Undoes the last commit, keeps the changes | No |
| `please redo` | Brings back the last undo | No |
| `please move-commit <branch>` | Moves the last commit onto a new branch | No |
| `please discard` | Throws away all uncommitted changes | Yes |
| `please restore <path>` | Brings back a file deleted in a past commit | No |
| `please branch delete <name>` | Deletes a branch locally and on origin | Yes |
| `please rename <new-name>` | Renames the current branch, including on the remote | No |
| `please cleanup` | Deletes local branches already merged into main | No |
| `please log` | A readable commit graph | No |
| `please revert` | Interactive revert of a past commit | No |
| `please stash` | Saves and clears the working tree | No |
| `please stash list` | Shows saved stashes | No |
| `please stash pop` | Restores the most recent stash | No |
| `please stash drop` | Deletes the most recent stash | Yes |
| `please "..."` | Agent mode, a plain language request | Varies |
| `please chat` | The agent, kept alive across multiple messages | Varies |
| `please alias <name>` | Gives please a shorter command name | No |

## Groups

{{< cards >}}
  {{< card link="commit" title="Commit" subtitle="please commit" icon="upload" />}}
  {{< card link="push" title="Push" subtitle="please push" icon="cloud-upload" />}}
  {{< card link="status" title="Status and Log" subtitle="status, log" icon="eye" />}}
  {{< card link="branch" title="Branches" subtitle="branch, switch, rename, cleanup, branch delete" icon="share" />}}
  {{< card link="sync" title="Sync" subtitle="sync, sync exactly" icon="refresh" />}}
  {{< card link="undo-redo" title="Undo and Redo" subtitle="undo, redo" icon="reply" />}}
  {{< card link="history" title="History Fixes" subtitle="revert, restore, move commit" icon="clock" />}}
  {{< card link="discard" title="Discard" subtitle="please discard" icon="trash" />}}
  {{< card link="stash" title="Stash" subtitle="stash, stash list, stash pop, stash drop" icon="archive" />}}
  {{< card link="agent-mode" title="Agent Mode" subtitle="please followed by a plain language request" icon="chip" />}}
  {{< card link="chat" title="Chat" subtitle="please chat" icon="chat-alt" />}}
  {{< card link="alias" title="Alias" subtitle="please alias" icon="tag" />}}
{{< /cards >}}
