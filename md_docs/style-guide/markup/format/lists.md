---
title: Lists
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup/format/lists/
---

# Lists

Lists are body elements that organize information into adjacent blocks of markup. Each level of a list must start and end with a blank line.

To learn more about when to use lists, see the Lists style guide entry.

## Unordered Lists

- Use hyphens (`-`) to indicate items in an unordered list.

- To create a multi-level list, indent each level two spaces for each subordinate level. Each subordinate level must start and end with a blank line.

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
- List item 1

  - List item 1a
  - List item 1b

- List item 2

  - List item 2a
  - List item 2b
```

</td>
<td headers="Avoid">
```rst
* List item 1
  - List item 1a
  - List item 1b

* List item 2
  - List item 2a
  - List item 2b
```

</td>
</tr>
</table>

## Ordered Lists

Ordered lists append a number before each item to show a sequential order.

- Use a number followed by a period for the first list item (`1.`, `a.`, and so on). This sets the numbering scheme you are using for this level of the list.

- Use a hash character followed by a period (`#.`) for each subsequent list item. The parser replaces the hash with the next number in the sequence.

- To create a multi-level list, indent each level three spaces for each subordinate level. Each subordinate level must start and end with a blank line.

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
1. List item 1

   a. List item 1a
   #. List item 1b

#. List item 2

   a. List item 2a
   #. List item 2b
```

</td>
<td headers="Avoid">
```rst
1. List item 1
   a. List item 1a
   b. List item 1b
2. List item 2
   a. List item 2a
   b. List item 2b
```

</td>
</tr>
</table>

## Definition Lists

Definition lists specify a term and a related block that you can use to describe the term.

To learn more about definition lists, see the Docutils documentation.