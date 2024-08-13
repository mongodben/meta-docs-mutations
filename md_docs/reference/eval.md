---
title: Eval Role
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/eval/
---

# Eval Role

This extension is both **experimental** and potentially slow.

You can execute an arbitrary Python expression using the `eval` role. This expression has access to the Python datetime module.

For example:

```rst
It is now
:eval:`int((datetime.datetime.now() - datetime.datetime(2010, 1, 1)).days / 365.2425)`
years since 2010.
```

eval.py