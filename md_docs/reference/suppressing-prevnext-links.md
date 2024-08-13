---
title: Suppressing Previous/Next Links
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/suppressing-prevnext-links/
---

# Suppressing Previous/Next Links

The MongoDB theme supports a `noprevnext`
metadata field which suppresses output of the previous page/next page links at the bottom of each page.

This is useful in cases where a user may be confused, such as in installation pages where the "next" link points to another platform's installation instructions.

For example:

```rst
:noprevnext:

==========================================
Install BI Connector on Debian-based Linux
==========================================

...
```