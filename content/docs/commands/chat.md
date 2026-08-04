---
title: please chat
weight: 11
---

The same agent as agent mode, kept alive across multiple messages instead of one and done.

<!--more-->

```text
$ please chat
> what changed since the last commit?
...
> undo that last one, actually
...
> good, now make a branch for the fix
...
> exit
```

Use `please "..."` for a single request. Switch to please chat when you want to go back and forth: ask a follow up, correct something, or build up a multi step task piece by piece, without repeating context each time.

Type exit or quit, or press Ctrl+D, to leave.

Same tools, same safety nets as agent mode. The only difference is that the conversation itself persists in memory for the life of the session, nothing is written to disk, so later messages can refer back to what was said or done earlier.
