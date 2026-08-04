---
title: please discard
weight: 8
---

Throws away all uncommitted changes, tracked and untracked.

<!--more-->

```bash
please discard
```

Replaces `git checkout -- .` followed by `git clean -fd`.

{{< callout type="warning" >}}
  This is destructive. please shows exactly what will be lost and requires typing yes to proceed.
{{< /callout >}}
