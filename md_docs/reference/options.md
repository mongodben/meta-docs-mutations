---
title: Options / Settings
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/options/
---

# Options / Settings

## Overview

Use `options-*.yaml` files to generate reference for MongoDB configuration settings (the ones that appear on Configuration File Options) and for binary / tools options.

`options-*.yaml` files generate consistently-formatted reference and let you single-source option descriptions that apply to multiple tools.

Giza builds an include file each entry in an `options-` YAML file (except those whose `program` field value begins with an underscore).

The generated file path (i.e. the file to include) is of the format

```none
/includes/option/{directive}-{program}-{name|filename}.rst
```

## Fields

- `program`: Name of the program to which the option/setting applies.

  If the value of the `program` field begins with an underscore (`_`), giza **will not** produce an include file. The MongoDB manual uses `program: _shared` for content that exists solely to be inherited into other files.

- `command`: Name of the command to which the option applies

- `name`: Name of the option/setting.

  If the directive is `option`, giza automatically prepends two dashes `-` to the beginning of the filename unless the first character of the name value is `<` or `-`.

  The following would therefore render as `--host`:

  ```yaml
  name: "host"
  ```

- `aliases`: Aliases for the option/setting. These are usually the short forms.

- `filename`: Specifies the name that giza should use when naming the generated include file.

  This supports documenting `-o` and `-O` for `mongostat`, since MacOS isn't case sensitive and thus was overwriting the first option file when generating the second.

- `args`": The arguments that the option accepts (e.g. `<host>:<port>`, `<timestamp>`, etc.). If there are no arguments, use `null`.

- `type`: The type of the option/setting (e.g. `string`, `non-negative integer`, etc.). Primarily used when documenting settings in `options-conf.yaml` in the manual.

- `directive`: The type of thing you're generating. Must be one of the following:

  - `option`

  - `setting`

  - `data`

  - `method`

  - `function`

  - `class`

  - `commandoption` (we should remove the code for this…)

  - other values that end in `setting`

- `pre`: a paragraph of text.

  The `pre` value will render as the **first paragraph** of the option/setting description.

  Use double-brace notation (`{{verb}}`) to facilitate content reuse. Specify the value for the variable using the `replacement` field or use a built-in variable

- `description`: A paragraph of text, usually the description of the option.

  Use double-brace notation (`{{verb}}`) to facilitate content reuse. Specify the value for the variable using the `replacement` field or use a built-in variable

- `post`: A paragraph of text.

  The `post` value will render as the **last paragraph** of text in the option/setting description.

  Use double-brace notation (`{{verb}}`) to facilitate content reuse. Specify the value for the variable using the `replacement` field or use a built-in variable.

- `default`

  The default for the option. When set, displays above the description paragraphs.

- `optional`: Indicates if the option/setting is optional.

  `optional` is currently broken and does not display anything in the generated include file.

- the following fields:

  - `name`: the name of the option/setting

  - `program`: the value of the `program` field of the option/setting that you wish to inherit

  - `file`: the path of the file containing the option/setting definition that you wish to inherit, relative to `source/includes/` (e.g. `options-shared.yaml`)

  When using `inherit`, you will need to overwrite, at a minimum, the inherited value for the `program` field.

- `replacement`: Lists the values to use in place of double-braced variables.

  You can overwrite the built-in variables in the `replacement` field or update custom variables declared using double-brace notation (`{{verb}}`).

  This field takes the following form:

  ```yaml
  replacement:
    - variable: "string with which to replace the variable"
  ```

- `edition`: Specifies the edition to which the option/setting applies. Could be used to support saas/onprem differences. Not currently used anywhere.

- `content`: Valid, but not currently used.

- `final`: Valid, but not currently used.

## Built-In Variables

- `{{role}}`: automatically replaced by a link to the option or setting (e.g. `mongod.--dbpath`).

- `{{program}}`: automatically replaced by the a link to the option or setting's specified `program` (e.g. `mongod`).

- `{{command}}`: automatically replaced by a link to the option or setting's specified `command` (e.g. `record`).

## Example

The following documents the `port` option used by the majority of MongoDB package components.

```yaml
program: _shared
name: port
args: <port>
default: 27017
directive: option
description: |
   {{intro}} TCP port on which the MongoDB instance listens for
   client connections.
optional: true
replacement:
  intro: "Specifies the"
```

Since the `program` value begins with an underscore, giza will not produce an include file for this entry.

The following *inherits* the `port` option definition, overwriting the `program` field value with `mongod`:

```yaml
program: mongod
name: port
inherit:
  name: port
  program: _shared
  file: options-shared.yaml
```

Giza will produce an include file at the path `/includes/option/option-mongod-port.rst`. The include file will resemble the following:

```rst
.. option:: --port <port>

   *Default*: 27017

   Specifies the TCP port on which the MongoDB instance listens for
   client connections.
```