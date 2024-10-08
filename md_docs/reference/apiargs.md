---
title: Apiargs
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/apiargs/
---

# Apiargs

## Overview

Use `apiargs-*.yaml` files to generate reference for the fields and parameters that methods, commands, aggregation pipeline stages, etc. accept.

Giza generates one table for each `apiargs-*.yaml` file. The table lists all of the arguments described in the YAML source.

The generated table is of the following format:

<table>

<tr>
<td>
`arg_name` (e.g. Parameter)

</td>
<td>
Type

</td>
<td>
Description

</td>
</tr>
<tr>
<td>
`<firstarg>`

</td>
<td>
`<type>`

</td>
<td>
Optional (if `optional: true`). <pre>

<description>

<post>

</td>
</tr>
</table>

## Filename Convention

Unlike options and extracts files, whose generated filenames depend on the *contents* of the YAML file, the generated `apiargs-` files are based off the source YAML filename itself.

By convention, `apiargs-*.yaml` filenames should be of the format:

```none
/includes/apiargs-<interface>-<operation>-<arg_name>.yaml
```

The generated file path (i.e. the file to include) is of the format

```none
/includes/apiargs/<string-that-came-after-apiargs--in-the-yaml-file-path>.rst
```

The arguments file for the parameters that the `db.collection.find()` method accepts would be:

```none
/includes/apiargs-method-db.collection.find-param.yaml
```

The path of the file to include is therefore:

```none
/includes/apiargs/method-db.collection.find-param.rst
```

## Fields

- `arg_name`: the variety of argument that you are documenting.

  Must be one of:

  - `param`: for parameters (the stuff you specify when calling the method/command/whatever). Displays in the table header as "Parameter".

    In the following, `pipeline` and `options` are parameters:

    ```sh
    db.collection.aggregate( pipeline, options )
    ```

  - `field`: for fields. Use `arg_name: field` to define a field you specify in a command invocation or to describe the fields accepted by the `options` parameter in a method. Displays in the table header as "Field".

  - `arg`: a generic argument (if you do not specify an `arg_name`, giza uses `arg` by default). Displays in the table header as "Argument".

  - `option`: valid but unused. Displays in the table header as "Option".

  - `flag`: valid but unused. Displays in the table header as "Flag".

- `interface`: the type of thing to which the argument belongs, such as `method`, `command`, `pipeline`, etc. *Not currently validated, so you can plop in whatever*.

- `operation`: the name of the method/command/pipeline stage/whatever to which the argument belongs (e.g. `db.collection.find()`).

- `name`: the name of the argument

- `type`: the datatypes that the argument accepts (e.g. `string`)

- `pre`: a paragraph of text.

  The `pre` value will render as the **first paragraph** of the table.

  Use double-brace notation (`{{verb}}`) to facilitate content reuse. Specify the value for the variable using the `replacement` field or use a built-in variable

- `description`: A paragraph of text, usually the description of the option.

  Use double-brace notation (`{{verb}}`) to facilitate content reuse. Specify the value for the variable using the `replacement` field or use a built-in variable

- `post`: A paragraph of text.

  The `post` value will render as the **last paragraph** of text in the table.

  Use double-brace notation (`{{verb}}`) to facilitate content reuse. Specify the value for the variable using the `replacement` field or use a built-in variable.

- `optional`: boolean indicating if the argument is optional. When `true`, giza prepends "Optional. " to the description section of the table.

- `position`: the order in which the argument should appear in the table. If you do not specify `position` values, Giza uses the order in which the arguments are listed in the YAML document.

- `replacement`: Lists the values to use in place of double-braced variables.

  You can overwrite the built-in variables in the `replacement` field or update custom variables declared using double-brace notation (`{{verb}}`).

  This field takes the following form:

  ```yaml
  replacement:
    - variable: "string with which to replace the variable"
  ```

- `source`: Use to inherit an argument from another file. `source` has the following fields:

  - `file`: the path of the file containing the argument that you wish to inherit, relative to `source/includes/` (e.g. `apiargs-method-db.collection.find-param.yaml`)

  - `ref`: the value of the `name` field of the argument that you wish to inherit.

## Built-In Variables

- `{{role}}`: automatically replaced by a link to the `operation`.

- `{{argname}}`: automatically replaced by the name of the argument.

In the following example, `{{role}}` would render as `db.collection.find()` and `{{argname}}` would render as `query`.

```yaml
arg_name: param
description: |
  {{argname}} Specifies selection filter using :doc:`query operators
  </reference/operator>`. To use {{role}} to retrieve all documents in
  a collection, omit this parameter or pass an empty document
  (``{}``).
interface: method
name: query
operation: db.collection.find
optional: true
position: 1
type: document
---
```

## Example

The following `apiargs-method-db.collection.find-param.yaml` file documents the parameters accepted by `db.collection.find()`.

```yaml
arg_name: param
description: |
  Specifies selection filter using :doc:`query operators
  </reference/operator>`. To return all documents in a collection, omit
  this parameter or pass an empty document (``{}``).
interface: method
name: query
operation: db.collection.find
optional: true
position: 1
type: document
---
arg_name: param
description: |
  Specifies the fields to return in the documents that match the
  query filter. To return all fields in the matching documents, omit this
  parameter.  For details, see :ref:`find-projection`.
interface: method
name: projection
operation: db.collection.find
optional: true
position: 2
type: document
...
```

Giza will produce an include file at the path `/includes/apairgs/method-db.collection.find-param.rst`. The include resembles the following:

```rst
.. only:: (html or singlehtml or dirhtml)

   .. list-table::
      :header-rows: 1
      :widths: 20 20 80

      * - Parameter

        - Type

        - Description

      * - ``query``

        - document

        - Optional. Specifies selection filter using :doc:`query operators
          </reference/operator>`. To return all documents in a collection, omit
          this parameter or pass an empty document (``{}``).

      * - ``projection``

        - document

        - Optional. Specifies the fields to return in the documents that match the
          query filter. To return all fields in the matching documents, omit this
          parameter.  For details, see :ref:`find-projection`.

.. only:: not(html or singlehtml or dirhtml)

   :param document query:

      Optional. Specifies selection filter using :doc:`query operators
      </reference/operator>`. To return all documents in a collection, omit
      this parameter or pass an empty document (``{}``).

   :param document projection:

      Optional. Specifies the fields to return in the documents that match the
      query filter. To return all fields in the matching documents, omit this
      parameter.  For details, see :ref:`find-projection`.
```