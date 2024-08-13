---
title: Source Constants
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/source-constants/
---

# Source Constants

The substitutions built into restructuredText have a number of limitations and quirks. For example, they cannot be used to substitute content inside of code blocks, and cannot contain links.

The MongoDB Documentation Project has an extension called `source_constants` which allows you to substitute constants anywhere in a page *before* docutils begins its parse stage.

## Example

In your `conf.py`, add `'source_constants'` to the `extensions` list, and define a `source_constants` dict:

```python
source_constants = {
    'package-branch': 'testing',
    'package-name-org': 'mongodb-org',
    'version': version
}
```

You may then use these constants in your restructuredText files:

```rst
Create the
``/etc/apt/sources.list.d/mongodb-org-4.4.0.list``
list file using the command appropriate for your version of Ubuntu:

.. code-block:: sh

   echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu \
        trusty/mongodb-org/testing multiverse" \
        | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
```

## Comparison with Other Variable Syntaxes

<table>
<tr>
<th id="">

</th>
<th id="4.0">
`4.0`

</th>
<th id="%7B%7Bversion%7D%7D">
`{{version}}`

</th>
<th id="%7Cversion%7C">
`|version|`

</th>
</tr>
<tr>
<td headers="">
Description

</td>
<td headers="4.0">
`source_constants`

</td>
<td headers="%7B%7Bversion%7D%7D">
Giza YAML substitutions

</td>
<td headers="%7Cversion%7C">
restructuredText substitutions

</td>
</tr>
<tr>
<td headers="">
Locations

</td>
<td headers="4.0">
Can be used anywhere

</td>
<td headers="%7B%7Bversion%7D%7D">
Can only be used within YAML files

</td>
<td headers="%7Cversion%7C">
May only be used in a subset of restructuredText syntactical locations

</td>
</tr>
<tr>
<td headers="">
Valid Content

</td>
<td headers="4.0">
Anything

</td>
<td headers="%7B%7Bversion%7D%7D">
Anything

</td>
<td headers="%7Cversion%7C">
May not be used to inject links or other non-trivial types of content

</td>
</tr>
<tr>
<td headers="">
Mutable

</td>
<td headers="4.0">
Can currently only be defined in `conf.py`

</td>
<td headers="%7B%7Bversion%7D%7D">
Yes. Can be overridden with Giza's content inheritance mechanism

</td>
<td headers="%7Cversion%7C">
Can only be defined once per page context

</td>
</tr>
<tr>
<td headers="">
Warns if undefined

</td>
<td headers="4.0">
Yes

</td>
<td headers="%7B%7Bversion%7D%7D">
No

</td>
<td headers="%7Cversion%7C">
Yes

</td>
</tr>
</table>