---
title: Markup Guidelines
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup-guidelines/
---

# Markup Guidelines

This page needs updated content and examples for MongoDB. Though incomplete, this page contains useful information and should be considered a resource though it is under revision.

This section describes markup conventions for reStructuredText (RST) and Markdown.

## reStructuredText (RST)

MongoDB documentation uses reStructuredText (RST) markup syntax with Sphinx extensions.

See Introduction to reStructured Text for more information on RST.

## Parts of reStructuredText

### Directives

A directive specifies a markup block-level element. Block-level elements span the entire width of a row within their container. The directives specify a UI element in which to format the associated text or content.

Docutils provides the following directives:

```rst
.. directive::

:role:
```