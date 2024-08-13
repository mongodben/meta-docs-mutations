---
title: Inline Markup
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup/inline/
---

# Inline Markup

Inline markup, also known as roles, specify how the enclosed text should be interpreted or rendered.

To learn more about roles, see the Docutils documentation.

Sphinx provides an extended set of roles. To learn more about the extended roles, see the Sphinx documentation.

## Font Formatting Roles

These roles control how the font of the enclosed text renders.

To learn more about when to use these roles, see the style guide section on Text Formatting.

- To **strongly emphasize** or **bold** text, use two asterisks on both sides of the text.

  ```rst
  **bold**
  ```

- To *emphasize* or *italicize* text, use one asterisk on both sides of the text.

  ```rst
  *italic*
  ```

- To specify `monospace` text, use two backticks on both sides of the text.

  ```rst
  ``monospace``
  ```

Use the following guidelines to avoid errors in font formatting roles:

- Don't start or end markup with whitespace.

  <table>
  <tr>
  <th id="Use">
  Use

  </th>
  <th id="Avoid">
  Avoid

  </th>
  </tr>
  <tr>
  <td headers="Use">
  ```rst
  **bold code**
  ```

  </td>
  <td headers="Avoid">
  ```rst
  ** bold code**
  ```

  </td>
  </tr>
  </table>

- Don't apply more than one type of markup to text.

  <table>
  <tr>
  <th id="Use">
  Use

  </th>
  <th id="Avoid">
  Avoid

  </th>
  </tr>
  <tr>
  <td headers="Use">
  ```rst
  ``bold code``
  ```

  </td>
  <td headers="Avoid">
  ```rst
  **``bold code``**
  ```

  </td>
  </tr>
  </table>

- When you apply a text formatting role to the middle of a word, use a backslash and space character on both sides of the formatted text.

  <table>
  <tr>
  <th id="Use">
  Use

  </th>
  <th id="Avoid">
  Avoid

  </th>
  </tr>
  <tr>
  <td headers="Use">
  ```rst
  this is *four* words

  thisis\ *one*\ word
  ```

  </td>
  <td headers="Avoid">
  ```rst
  thisis*one*word
  ```

  </td>
  </tr>
  </table>