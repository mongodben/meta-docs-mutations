---
title: Dates
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/dates/
---

# Dates

Dates are displayed differently in different countries, so you must use a date format that's explicit and consistent and that global users can't misinterpret.

Unless space is limited, always show dates in the following format: *month day*, *year*. Always spell out the month.

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
November 12, 2010

</td>
<td headers="Avoid">
12 Nov 2010

2010-Nov-12

11/12/2010

11/12/10

12/11/10

10-11-12

</td>
</tr>
</table>Don't use ordinal numbers for dates. For example, don't use *January 1st*; use *January 1* instead.

When the month, day, and year are embedded in a sentence, use a comma before and after the year. When only the month and year are embedded in a sentence, omit the commas unless the syntax would ordinarily require a comma following the year.

<table>
<tr>
<th id="Use">
Use

</th>
</tr>
<tr>
<td headers="Use">
Any sites that are using MySQL 4 after November 1, 2011, will be automatically migrated to MySQL 5.

</td>
</tr>
<tr>
<td headers="Use">
The Alert Logic Security Research Team used 12 months of security event data captured from July 2010 through June 2011.

</td>
</tr>
<tr>
<td headers="Use">
As of September 2013, a subset of customer accounts weren't being billed for actual usage in comparison to their preselected SQL Server storage allocations.

</td>
</tr>
</table>Use an all-numeric date only in the following situations:

- Space is limited, as in a table or figure.

- You need to show a literal representation of the date as it's displayed in the software.

Because all-numeric dates are interpreted differently in different countries, explain the format of a numeric date, and use a consistent format throughout the documentation. If possible, use the ISO 8601 format, which is *yyyy*-*mm*-*dd* (for example, 2012-11-10 for November 10, 2012).

<table>
<tr>
<th id="Use">
Use

</th>
</tr>
<tr>
<td headers="Use">
The value that's shown for 8/19/10 represents the average number of extents from data collections beginning August 19, 2010.

</td>
</tr>
</table>For information about and examples for showing a date range, see Ranges of Numbers.