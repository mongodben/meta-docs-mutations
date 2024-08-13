---
title: cond Directive
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/cond/
---

# `cond` Directive

The Sphinx built-in `only` directive allows writers to conditionally include content based on a set of *tags* specified at build-time. The MongoDB documentation project uses this primarily to differentiate between prose intended for Ops Manager and that intended for Cloud Manager.

However, even if a block of content is supressed by `only`, Sphinx still *evaluates* it. This leads to surprising behavior when sections and references are defined within a conditional block.

As a workaround, you may use the experimental `fixed_only` extension containing the `cond` directive.

This directive uses the same syntax as `only`, but does **not** evaluate suppressed content.

```rst
Access :guilabel:`Data Explorer`
--------------------------------

.. cond:: cloud

   .. note::

      To access :guilabel:`Data Explorer`, you must have been
      granted access through one of the following roles:

      - :authrole:`Project Owner` or
        :authrole:`Organization Owner`

      - :authrole:`Project Data Access Admin`

      - :authrole:`Project Data Access Read/Write`

      - :authrole:`Project Data Access Read Only`

      Data Explorer is not available for trial versions of |mms|
      after the initial 30 day trial period.

.. cond:: onprem

   .. note::

      To access :guilabel:`Data Explorer`, you must have been
      granted access through one of the following roles:

      - :authrole:`Project Owner` or
        :authrole:`Organization Owner`

      - :authrole:`Project Data Access Admin`

      - :authrole:`Project Data Access Read/Write`

      - :authrole:`Project Data Access Read Only`
```