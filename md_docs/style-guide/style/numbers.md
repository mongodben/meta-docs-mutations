---
title: Numbers
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/numbers/
---

# Numbers

Use the following guidelines for showing numbers in documentation.

## Numbers versus Words

Spell out numbers from zero through nine, except in the cases shown in the following table. In these cases, or if the number is 10 or larger, use numerals.

<table>
<tr>
<th id="Exception">
Exception

</th>
<th id="Example">
Example

</th>
</tr>
<tr>
<td headers="Exception">
Numbers as they're displayed

</td>
<td headers="Example">
The returned value is 0.

</td>
</tr>
<tr>
<td headers="Exception">
Numbers to use as input

</td>
<td headers="Example">
Type **1** and press **Enter**.

</td>
</tr>
<tr>
<td headers="Exception">
Series of the same type of items where at least one of the numbers is greater than nine

</td>
<td headers="Example">
Unit A requires 5 nodes, Unit B requires 17 nodes, and Unit C requires 9 nodes.

</td>
</tr>
<tr>
<td headers="Exception">
Numbers with symbols

</td>
<td headers="Example">
7%

</td>
</tr>
<tr>
<td headers="Exception">
Numbers with units of measure or abbreviations

</td>
<td headers="Example">
5 mm, 3-inch disk

</td>
</tr>
<tr>
<td headers="Exception">
Numbers that indicate dimensions

</td>
<td headers="Example">
8x8 feet

</td>
</tr>
<tr>
<td headers="Exception">
Time

</td>
<td headers="Example">
5:45 p.m.

</td>
</tr>
</table>Avoid beginning a sentence with a number. If you must begin a sentence with a number, spell out the number unless the number is part of a product, service, or company name.

<table>
<tr>
<th id="Use">
Use

</th>
</tr>
<tr>
<td headers="Use">
Ten vendors, including MongoDB, were assessed based on the following attributes:

451 Research applied a weighting system to highlight the attributes that are most valued by end users.

</td>
</tr>
</table>Don't use the spelled-out form of a number followed by a numeral in parentheses. However, if you think that a user might misread the numeral 0 as the letter O, you can clarify by spelling out zero parenthetically after the numeral.

<table>
<tr>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Use">
two panels

zero probability

Enter **0** (zero). *(acceptable)*

</td>
<td headers="Don't%20use">
two (2) panels

zero (0) probability

</td>
</tr>
</table>

## Commas in Numbers

Use commas in numbers with five or more digits. However, don't use commas in the following types of numbers:

- Addresses

- Fractional part of a decimal number

- Page numbers

- Literal representations of user-entered values or displayed values

<table>
<tr>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Use">
9001 N IH 35

1452.7532

page 1055

1024 bytes

</td>
<td headers="Don't%20use">
9,001 N IH 35

1,452.753,2

page 1,055

1,024 bytes

</td>
</tr>
</table>Don't use European-style numbering, which uses commas in the place of periods. For example, use 3.14159, not 3,14159.

## Ranges of Numbers

When describing number ranges, use the following guidelines:

- To describe an inclusive range, use *through*. When space is limited, use an en dash instead. Don't use the word *inclusive* in your description.

- Use prepositions as follows:

  - If you use *between* to introduce a range, use *and* to conclude the range. Using *between* and *and* implies a noninclusive range.

  - If you use *from* to introduce a range, use *through* or *to* to conclude the range.

  - Don't mix *between* or *from* with an en dash.

<table>
<tr>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Use">
step 12 through step 16 options 11–15 *(limited space)* any value from 1 through 258

</td>
<td headers="Don't%20use">
step 12 through step 16, inclusive

</td>
</tr>
<tr>
<td headers="Use">
from 10 to 20 diagrams

</td>
<td headers="Don't%20use">
from 10–20 diagrams

</td>
</tr>
<tr>
<td headers="Use">
between 2010 and 2012

</td>
<td headers="Don't%20use">
between 2000–2002

</td>
</tr>
</table>

## Unspecified, Generic, and Unknown Numbers

To represent an unspecified or generic number, use *n* as the variable and apply italics.

To represent an unspecified or unknown version number, use *x* for each digit and apply italics.

<table>
<tr>
<th id="Use">
Use

</th>
</tr>
<tr>
<td headers="Use">
Move the insertion point *n* spaces to the right.

Select the **Use n I/O Sessions** check box.

Your BlackBerry software must be version 4. *x*.

</td>
</tr>
</table>