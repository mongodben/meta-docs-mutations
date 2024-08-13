---
title: XML Role
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/xmlrole/
---

# XML Role

The docutils restructuredText parser does not support nesting roles or formatting markup. This makes it impossible to, for example, have a monospace-formatted `ref` link without making a sphinx extension providing each possible permutation of formatting.

The `xml` role in the `xmlrole` extension allows you to express formatting using XML. It accepts the following tags:

<table>
<tr>
<th id="Tag">
Tag

</th>
<th id="Attributes">
Attributes

</th>
<th id="Description">
Description

</th>
</tr>
<tr>
<td headers="Tag">
`em`

</td>
<td headers="Attributes">

</td>
<td headers="Description">
Emphasize the contained text. Typically renders as italics.

</td>
</tr>
<tr>
<td headers="Tag">
`mono`

</td>
<td headers="Attributes">

</td>
<td headers="Description">
Render the contained text in a monospace font.

</td>
</tr>
<tr>
<td headers="Tag">
`strong`

</td>
<td headers="Attributes">

</td>
<td headers="Description">
Render the contained text in a bold font.

</td>
</tr>
<tr>
<td headers="Tag">
`ref`

</td>
<td headers="Attributes">
`target=<ref>`

</td>
<td headers="Description">
Create a link to the docutils reference indicated by `target`.

</td>
</tr>
<tr>
<td headers="Tag">
`link`

</td>
<td headers="Attributes">
`target=<url>`

</td>
<td headers="Description">
Create a link to a URL indicated by `target`.

</td>
</tr>
</table>For example:

```rst
:xml:`<mono><ref target="binary-bson-dumps"></ref></mono>`

:xml:`<strong>See: <link target="https://example.com">An Example Link</link></strong>`
```

xmlrole.py