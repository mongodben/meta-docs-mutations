---
title: Placeholder or Variable Text
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/placeholder-variable-text/
---

# Placeholder or Variable Text

Use placeholder text for a value when you:

- Don't know its specific value

- Don't or shouldn't use an example value

Use placeholders when demonstrating how a command or path should be constructed. Users supply the relevant value for the placeholder when using the command or syntax. When using placeholders, instruct users to replace the placeholders with the relevant values.

Placeholder text is also referred to as *variable text* or *replaceable text*.

Placeholder text usually indicates the type of element that's being represented. For example, *directoryName* would likely indicate the name of a directory.

## Placeholder Text Guidelines

When creating placeholder text, use the following guidelines.

To learn about showing placeholders for API resources, see API Placeholders.

<table>
<tr>
<th id="Guidelines">
Guidelines

</th>
<th id="Example">
Example

</th>
</tr>
<tr>
<td headers="Guidelines">
Use the `.. code-block:: <lexer>` for multiline code examples.

As you can't apply text formatting to the code, enclose placeholders in punctuation that doesn't have any other special use in the code. Use a consistent convention throughout the documentation set per the programming language.

</td>
<td headers="Example">
```rst
.. code-block:: console

   mongod --port <portNumber> \
          --dbpath <tempDatabasePath> \
          --setParameter ttlMonitorEnabled=false
```

```console
mongod --port <portNumber> \
       --dbpath <tempDatabasePath> \
       --setParameter ttlMonitorEnabled=false
```

</td>
</tr>
<tr>
<td headers="Guidelines">
Use lowercase letters except when showing a multiple-word placeholder.

To show a multiple-word placeholder:

- Don't separate the words with spaces or symbols

- Capitalize the first letter of each word after the first word (called camelCase)

- Never capitalize the first word

Use lowercase and camelCase unless you need to follow the conventions of the programming language.

</td>
<td headers="Example">
*password*, *eventTypeName*, *apiKey*, *hostId*

</td>
</tr>
<tr>
<td headers="Guidelines">
Use one or more whole words to represent a placeholder.

- Don't sacrifice clarity for brevity.

- Create descriptive and meaningful placeholders.

</td>
<td headers="Example">
*device*; not *dev*

*installationDirectory*; not *installDir*

*mode*; not *########* (a series representing a number of digits)

</td>
</tr>
</table>

## Placeholder Explanation Guidelines

When explaining a placeholder, use the following guidelines:

<table>
<tr>
<th id="Guideline">
Guideline

</th>
<th id="Example">
Example

</th>
</tr>
<tr>
<td headers="Guideline">
Use a sentence to describe the placeholder parameter.

</td>
<td headers="Example">
```console
mongod --port <portNumber> \
       --dbpath <tempDatabasePath> \
       --setParameter ttlMonitorEnabled=false
```

*port* is the unique number for the `mongod` service. The default value is `27017`.

</td>
</tr>
<tr>
<td headers="Guideline">
Use a table if you need to explain two or more placeholders. This table should provide the parameter, data type, necessity (*required*, *optional*, or *conditional*), and a description of that parameter.

</td>
<td headers="Example">
```console
mongod --port <portNumber> \
       --dbpath <tempDatabasePath> \
       --setParameter ttlMonitorEnabled=false
```

<table>
<tr>
<th id="Parameter">
Parameter

</th>
<th id="Type">
Type

</th>
<th id="Necessity">
Necessity

</th>
<th id="Description">
Description

</th>
</tr>
<tr>
<td headers="Parameter">
dbpath

</td>
<td headers="Type">
string

</td>
<td headers="Necessity">
Required

</td>
<td headers="Description">
Root-relative file path for the temporary database.

</td>
</tr>
<tr>
<td headers="Parameter">
port

</td>
<td headers="Type">
integer

</td>
<td headers="Necessity">
Required

</td>
<td headers="Description">
Unique number for this `mongod` service. The default value is `27017`.

</td>
</tr>
<tr>
<td headers="Parameter">
setParameter

</td>
<td headers="Type">
array

</td>
<td headers="Necessity">
Required

</td>
<td headers="Description">
List of key-value pairs that pass instructions to the `mongod` service.

</td>
</tr>
</table>

</td>
</tr>
<tr>
<td headers="Guideline">
Avoid standalone clauses that begin with *where*.

</td>
<td headers="Example">
```console
mongod --port <portNumber> \
       --dbpath <tempDatabasePath> \
       --setParameter ttlMonitorEnabled=false
```

where *port* is the unique number for the `mongod` service. The default value is `27017`.

</td>
</tr>
</table>