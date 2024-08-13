---
title: Fantastic Errors and How to Fix Them
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/error-kb/
---

# Fantastic Errors and How to Fix Them

<table>

<tr>
<td>
Error

</td>
<td>
Resolution

</td>
</tr>
<tr>
<td>
`Duplicate explicit target name`

</td>
<td>
This is most frequently caused by improper use of *named hyperlink references*. Instead, use an *anonymous hyperlink reference*.

For example, instead of this:

```rst
`Foo <http://example.org>`_
```

Use this:

```rst
`Foo <http://example.org>`__
```

</td>
</tr>
</table>