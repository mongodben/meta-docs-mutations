---
title: Headings and Sections
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup/headings/
---

# Headings and Sections

Headings organize information into a hierarchy of sections. To set headings, add repeating characters below the heading text.

To learn more about headings, see the Sphinx documentation.

## Heading Markup Rules

To avoid errors in your header markup syntax, stick to the following rules:

- Don't skip heading levels. Heading level 3 can't come after heading level 1.

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
  ============
  Manage Users
  ============

  Create One New User
  -------------------

  Options
  ~~~~~~~
  ```

  </td>
  <td headers="Avoid">
  ```rst
  ============
  Manage Users
  ============

  Create One New User
  ~~~~~~~~~~~~~~~~~~~
  ```

  </td>
  </tr>
  </table>

- Make the underline as long as the text above it. If you use a source constant in the header, the underline must match the length of the resolved text.

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
  Create One New User
  -------------------
  ```

  </td>
  <td headers="Avoid">
  ```rst
  Create One New User
  ----------------
  ```

  </td>
  </tr>
  <tr>
  <td headers="Use">
  This example assumes the source constant `{+db+}` resolves to "Database".

  ```rst
  {+db+} Functions
  ------------------
  ```

  </td>
  <td headers="Avoid">
  ```rst
  {+db+} Functions
  ---------------
  ```

  </td>
  </tr>
  </table>