---
title: Shared Include
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup/directives/sharedinclude/
---

# Shared Include

The `sharedinclude` directive lets you source content from a file located in the MongoDB internal docs-shared repository. Use this directive when you need to keep the same content in sync for multiple sets of documentation or branches of a documentation set.

This page uses the following terms:

Content committed to the `docs-shared` repository that other documentation repositories can source.

Content in a documentation repository that uses a `sharedinclude` directive to pull content from an external file.

Variable that identifies where replacement content should be inserted. These variables are represented as a name surrounded by the `|` (pipe) character. Add them in the external file and define the replacement content in the sourcing file.

The `sharedinclude` directive extends the `include` directive. While the `include` directive allows you to source content from the branch of the repository in which it is used, the `sharedinclude` directive is hard-coded to reference external files from the 10gen/docs-shared private GitHub repository.

## Setup

You must ensure the `sharedinclude_root` setting in the documentation repository's `snooty.toml` configuration file is set to the shared content repository URL. This URL must point to the unprocessed version of the files currently served from the `raw.githubusercontent.com` domain.

For example, if the external files that your docs repository file references is on the `main` branch of `docs-shared`, your docs repository `snooty.toml` configuration entry should resemble the following line:

```
sharedinclude_root = "https://raw.githubusercontent.com/10gen/docs-shared/main/"
```

Snooty reports an error if you attempt to use `sharedinclude` without configuring this setting.

## Syntax

Add the `sharedinclude` directive to the sourcing file to include content from the external file.  Specify the path of the external file relative to the `docs-shared` base directory, omitting the leading slash.

For example, if the file path from the root of the `docs-shared` repository is `drivers/compatibility-tables/c.rst`, the RST in the sourcing file should include the following code:

```rst
.. _sharedinclude:: drivers/compatibility-tables/c.rst
```

The external file includes replacement variables in the form of `|variable-name|`. You can define the replacement values in sourcing files to customize segments of the page.

For example, suppose the `docs-shared` file `language.rst` contained the following content with a replacement variable called `|driver-name|`:

```rst
The following table shows the compatibility between different versions of
the |driver-name| driver and the |driver-language|:
```

The sourcing file could resemble the following code:

```rst
 :caption: compatibility-table.txt sourcing file in the documentation repository
 :copyable: false
.. _sharedinclude:: drivers/compatibility-tables/language.rst

   .. replacement:: driver-name

      PyMongo

   .. replacement:: driver-language

      Python language
```

The published page displays the following text:

```rst
The following table shows the compatibility between different versions of
the PyMongo driver and the Python language:
```

Snooty reports a warning or error if the sourcing file is missing any replacement variables present in the external file.

### Placeholders in Inline Context

An **inline context** describes the positioning of placeholders as adjacent to other paragraph text. If the placeholder is in an inline context, you can replace it with markup elements, including the following types:

- Unformatted text

- Formatted text such as `monospace`, **emphasis**, or *italic*

- Links

You cannot replace variable placeholders in inline contexts with elements such as lists, code blocks, includes, and headers. If you need to source these elements from a `sharedinclude`, ensure the placeholders are in a block context as described in the next section.

For example, suppose you want to source content from an external file, located at `dbx/fundamentals/agg-operators.rst` in the `docs-shared` repository that contains the following content:

```rst
To learn more about **aggregation operators**, see the
|learn-agg-operator-docs|.
```

In the sourcing file, you can use the following placeholder replacement in the `sharedinclude` directive:

```rst
.. sharedinclude:: dbx/fundamentals/agg-operators.rst

   .. replacement:: learn-agg-operator-docs

      Aggregation Operations page in the
      :server:`MongoDB Server documentation </aggregation>`
```

The published page renders as if the sourcing file contained the following RST:

```rst
To learn more about **aggregation operators**, see the Aggregation Operations
page in the :server:`MongoDB Server documentation </aggregation>`.
```

### Placeholders in Block Context

A **block context** describes the positioning of placeholders as separated from paragraph text by line breaks. You can replace placeholders in a block context with most inline or block RST elements, including the following types:

- Titles

- Code blocks

- Anchors

- Admonitions

For example, suppose you want to source content from an external file located at `dbx/fundamentals/agg-operators.rst` in the `docs-shared` repository, which contains the following content:

```rst
The following section demonstrates how to use aggregation operators to build
an aggregation pipeline.

|aggregation-operators-example|

To learn more, see ...
```

In the sourcing file, you can use the following placeholder replacement in the `sharedinclude` directive:

```rst
.. sharedinclude:: dbx/fundamentals/agg-operators.rst

   .. replacement:: aggregation-operators-example

      .. _expression-operators-example:

      Expression Operators Example
      ````````````````````````````

      Expression operators are similar to functions and can take an array
      of arguments as shown in the following format:

      .. code-block::

         { <operator>: [ <argument1>, <argument2> ... ] }
```

The published page renders as if the sourcing file contained the following RST:

```rst
The following section demonstrates how to use aggregation operators to build
an aggregation pipeline.

.. _expression-operators-example:

Expression Operators Example
````````````````````````````

Expression operators are similar to functions and can take an array
of arguments as shown in the following format:

.. code-block::

   { <operator>: [ <argument1>, <argument2> ... ] }

To learn more, see ...
```