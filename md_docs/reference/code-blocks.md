---
title: Code Examples
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/code-blocks/
---

# Code Examples

Snooty supports the following directives for code samples:

- `code-block`

- `io-code-block`

- `literalinclude`

These directives feature a monospace font and syntax highlighting that makes source code easier to interpret.

## Code Blocks

The `code-block` directive formats a code sample with the following options.

### Syntax

```
.. code-block:: <language>
   :copyable: <boolean>
   :emphasize-lines: <line numbers>
   :linenos:
   :caption: <caption text>
   :source: <url>

   <code sample>
```

### Options

All of the following options are optional.

<table>

<tr>
<td>
`<language>`

</td>
<td>
Language to use for syntax highlighting.

For a complete list of supported languages, see the leafygreen-ui GitHub repository.

**Default:** None

</td>
</tr>
<tr>
<td>
`:copyable: <boolean>`

</td>
<td>
Option that indicates whether to show the copy icon.

**Default:** `true`

</td>
</tr>
<tr>
<td>
`:emphasize-lines: <line number>`

</td>
<td>
Lines to highlight. You can specify a range of line numbers, individual line numbers, or both.

**Default:** None

</td>
</tr>
<tr>
<td>
`:linenos:`

</td>
<td>
Option that indicates whether to show line numbers.

**Default:** None

</td>
</tr>
<tr>
<td>
`:caption: <caption text>`

</td>
<td>
Brief description.

**Default:** None

</td>
</tr>
<tr>
<td>
`:source: <url>`

</td>
<td>
Option that indicates whether to show the source icon and View full source tooltip.

This icon is hidden if the `copyable` option is set to `false`.

**Default:** None

</td>
</tr>
</table>

### Example 1

```
.. code-block:: python
   :linenos:
   :copyable: true
   :emphasize-lines: 1, 4-5
   :caption: An example Python code block

   print("Hello Docs team!")
   print("This is Python code...")
   print("...inside a code-block.")
   print("The line numbers are over here <-")
   print("And the copy icon is over there ->")
```

The previous `code-block` directive creates the following output:

```python
print("Hello Docs team!")
print("This is Python code...")
print("...inside a code-block.")
print("The line numbers are over here <-")
print("And the copy icon is over there ->")
```

### Example 2

```
.. code-block:: python
   :source: https://github.com/mongodb/docs-ecosystem/blob/36f9cc7260a246d47cb05ac35276a2c92734b028/conf.py#L120

   html_theme = sconf.theme.name
   html_theme_path = [os.path.join(conf.paths.buildsystem, 'themes')]
   html_title = conf.project.title
   htmlhelp_basename = 'MongoDBdoc'
```

The previous `code-block` directive creates the following output:

```python
html_theme = sconf.theme.name
html_theme_path = [os.path.join(conf.paths.buildsystem, 'themes')]
html_title = conf.project.title
htmlhelp_basename = 'MongoDBdoc'
```

## I/O Code Blocks

The `io-code-block` directive formats a code sample and includes an expandable code block for the output and a button to toggle its visibility.

### Syntax

```
.. io-code-block::
   :copyable: <boolean>
   :caption: <caption text>
   :source: <url>

   .. input::
      :language: <input language>
      :emphasize-lines: <line numbers>
      :linenos:

      <input code>

   .. output::
      :language: <output language>
      :emphasize-lines: <line numbers>
      :linenos:
      :visible: <boolean>

      <output code>
```

### Options

All of the following options are optional.

<table>

<tr>
<td>
`:copyable: <boolean>`

</td>
<td>
Option that indicates whether to show the copy icon for the input code.

**Default:** `false`

</td>
</tr>
<tr>
<td>
`:language:`

</td>
<td>
Language to use for syntax highlighting. You can specify different languages for the input and output code.

For a complete list of supported languages, see the leafygreen-ui GitHub repository.

**Default:** None

</td>
</tr>
<tr>
<td>
`:linenos:`

</td>
<td>
Option that indicates whether to show line numbers.

**Default:** None

</td>
</tr>
<tr>
<td>
`:emphasize-lines: <line number>`

</td>
<td>
Lines to highlight. You can specify a range of line numbers, individual line numbers, or both.

**Default:** None

</td>
</tr>
<tr>
<td>
`:visible: <boolean>`

</td>
<td>
Option that indicates whether the output code is initially visible. If `false`, the user must click a button to see the output.

**Default:** `true`

</td>
</tr>
<tr>
<td>
`:caption: <caption text>`

</td>
<td>
Brief description.

**Default:** None

</td>
</tr>
<tr>
<td>
`:source: <url>`

</td>
<td>
Option that indicates whether to show the source icon and View full source tooltip.

This icon is hidden if the `copyable` option is set to `false`.

**Default:** None

</td>
</tr>
</table>

### Example 1

```
.. io-code-block::
   :copyable: true
   :caption: An example Python code block with output

   .. input::
      :language: python
      :emphasize-lines: 1
      :linenos:

      print("Hello Docs team!")
      print("This is Python code...")
      print("...inside an io-code-block.")

   .. output::
      :language: shell
      :emphasize-lines: 1
      :linenos:
      :visible: false

      "Hello Docs team!"
      "This is Python code..."
      "...inside an io-code-block."
```

```python
print("Hello Docs team!")
print("This is Python code...")
print("...inside an io-code-block.")
```

```shell
"Hello Docs team!"
"This is Python code..."
"...inside an io-code-block."
```

### Example 2

```
.. io-code-block::
   :source: https://github.com/mongodb/docs-node/blob/0cf95d4eac536ed0ae1a2085948dd98f24ac48af/source/quick-reference.txt#L473
   :copyable: true

   .. input::
      :language: javascript

      coll.find({ $text: { $search: 'zissou' } });

   .. output::
      :language: javascript

      [
          { title: 'The Life Aquatic with Steve Zissou', ... }
      ]
```

The previous `io-code-block` directive creates the following output:

```javascript
coll.find({ $text: { $search: 'zissou' } });
```

```javascript
[
    { title: 'The Life Aquatic with Steve Zissou', ... }
]
```

## Literal Includes

The `literalinclude` directive includes and formats a code example from another file. You can specify the comments or other lines of code on which to start and end the example. This directive allows you to maintain the code in a separate single file and display the same code example in multiple places.

Use the `literalinclude` directive to include a code file in the docs. Use the `include` directive to include an `rst` file in the docs.

### Syntax

```
.. literalinclude:: <file path>
   :language: <language>
   :copyable: <boolean>
   :start-after: <line of code>
   :end-before: <line of code>
   :linenos:
   :lineno-start: <line number>
   :emphasize-lines: <line numbers>
   :caption: <caption>
   :dedent: <number>
```

### Options

<table>

<tr>
<td>
`<file path>`

</td>
<td>
**Required.** Path to the file in the repository that contains the code to show.

**Default:** None

</td>
</tr>
<tr>
<td>
`:language: <language>`

</td>
<td>
Language to use for syntax highlighting.

For a complete list of supported languages, see the leafygreen-ui GitHub repository.

**Default:** None

</td>
</tr>
<tr>
<td>
`:copyable: <boolean>`

</td>
<td>
Option that indicates whether to show the copy icon.

**Default:** `true`

</td>
</tr>
<tr>
<td>
`:start-after: <line of code>`

</td>
<td>
Line of code before the first line to include in the sample.

You can use a comment to mark the point where the `literalinclude` directive starts including code. If you do, omit the comment marker (`#` or `//`) from the attribute value.

By using comments, you can unambiguously specify the start of the code example, regardless of how many examples you're including from the file. You also won't need to update the directive if the extracted code changes.

**Default:** Beginning of file

</td>
</tr>
<tr>
<td>
`:end-before: <line of code>`

</td>
<td>
Line of code after the last line to include in the sample.

You can use a comment to mark the point where the `literalinclude` directive stops including code. If you do, you can omit the comment marker (`#` or `//`) from the attribute value.

By using comments, you can unambiguously specify the end of the code sample, regardless of how many examples you're including from the file. You also won't need to update the directive if the extracted code changes.

**Default:** End of file

</td>
</tr>
<tr>
<td>
`:linenos:`

</td>
<td>
Option that indicates whether to show line numbers.

**Default:** None

</td>
</tr>
<tr>
<td>
`:lineno-start:`

</td>
<td>
Number of the line at which to start showing line numbers. This option requires the `:linenos:` option.

**Default:** 1

</td>
</tr>
<tr>
<td>
`:emphasize-lines: <line number>`

</td>
<td>
Lines to highlight. You can specify a range of line numbers, individual line numbers, or both.

**Default:** None

</td>
</tr>
<tr>
<td>
`:caption: <caption text>`

</td>
<td>
Brief description.

**Default:** None

</td>
</tr>
<tr>
<td>
`:dedent: <number of spaces>`

</td>
<td>
Number of spaces to remove from the beginning of each line of code. Use this option if the code to show is indented in the code file.

**Default:** None

</td>
</tr>
</table>

### Example 1

Suppose you want to include samples from the following Python file in a documentation page:

```python
print("Hello Docs team!")
print("This is Python code...")
print("...in another file.")
print("This line will be included in the docs...")
print("...but this line won't.")

def sample_function():
  # start-function-sample
  print("This sample has comments to mark the extract start and end.")
  # end-function-sample
  print("This line won't be included in the sample.")
```

The following `literalinclude` directive starts with the first line of the file and ends before the line that reads `print("...but this line won't.")`:

```
.. literalinclude:: /includes/python-sample.py
   :copyable: false
   :end-before: print("...but this line won't.")
   :caption: Sample Python code from another file
```

The previous `literalinclude` directive creates the following output:

```
print("Hello Docs team!")
print("This is Python code...")
print("...in another file.")
print("This line will be included in the docs...")
```

### Example

In the Python file in the previous example, the code inside `sample_function()` is indented two spaces. The following `literalinclude` directive uses the `:dedent:` option to remove these spaces:

```
.. literalinclude:: /includes/python-sample.py
   :start-after: start-function-sample
   :end-before: end-function-sample
   :linenos:
   :lineno-start: 9
   :dedent: 2
```

The previous directive creates the following output:

```
print("This sample has comments to mark the extract start and end.")
```