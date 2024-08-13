---
title: Tables
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/tables/
---

# Tables

Text that's difficult to read in paragraph form often becomes clearer when put into a table. Tables are easy to scan. They clarify the relationships between portions of information on the page. This topic provides the guidelines for the following aspects of tables:

- Introductory Text for Tables

- Table Titles

- Column Headers

- Table Text

- Table Footnotes

- Attribute or Parameter Tables in API documents

- Examples

Don't create tables that are overly complex or that scroll horizontally. If a table has too much information, try to break it up into smaller tables.

## Introductory Text for Tables

In the text that precedes a table, introduce the table in a way that relates the table to the text. If the table immediately follows the reference to it, use a generic reference (such as *the following table*) even if the table has a title. Provide a link to a table title only when the table doesn't immediately follow the reference or when the table is in a different article or section.

To introduce a table, use a sentence (not a fragment), and end the sentence with a colon.

## Table Titles

Tables in conceptual topics should normally have titles (captions). However, some tables are closely associated with the surrounding text and don't require titles. For example, decision matrixes and tables within tasks, procedures, and tutorials don't require titles.

When creating table titles, use the following guidelines:

- Use headline-style capitalization for table titles. To learn more, see Titles and Headings.

- Don't start a table title with an article (*a*, *an*, *the*).

- Don't end a table title with a period or colon.

- Place the title above the table, not below it, and format it in **boldface**.

- Don't number table titles.

- Make table titles concise; limit them to one line if possible.

- Make table titles descriptive:

  - Avoid using a table title that duplicates a topic or section title.

  - Ensure that no two table titles in an article or section are identical. To distinguish between the titles that are similar, add qualifiers.

- Don't include trademark symbols in table titles.

## Column Headers

Use the following guidelines for text in column headers:

- Use headline-style capitalization in column headers. However, for words that are always uppercase or always lowercase, match that case.

- Use singular nouns for column headers, unless the context requires otherwise.

- Don't end column headers with ellipses or colons.

## Table Text

Use the following guidelines for text in table cells:

- Use the same punctuation and capitalization guidelines that you use for text in lists. See List Items.

- Make the entries in a table parallel. For example, in a column that describes options, be consistent in beginning the entries with a verb or noun.

- Avoid leaving a table cell blank. If no information is available for that cell, use *Not applicable* or *None*. Use the abbreviation *NA* only if space constraints exist. Don't use dashes. An exception is for matrix-type tables that use an X or other marker to indicate support. In such cases, blank cells are acceptable (see the third example at the end of this topic).

- When showing a callout (for example, a note or warning) in a table, use the guidelines in Callouts and Admonitions.

- If space in a table is constrained, you can use abbreviations and symbols that you wouldn't normally use in body text (such as % for percent).

- Don't use color to differentiate table text.

## Table Footnotes

If a callout (for example, a note or warning) applies to the entire table, place the content in a regular callout preceding the table. If a callout applies only to the content in a certain cell, place the callout in that cell. However, if a callout applies to all of the content in a row or column, or to the content in two or more cells, you can use footnotes.

- When writing the text of table footnotes, use the following guidelines:

  - Ensure that all footnotes are written clearly and completely. Use sentences when possible. Avoid cryptic language.

  - Ensure that all footnotes have parallel grammatical structure (sentences are paralleled by sentences, phrases by phrases, and so on).

- Place the footnote text at the end of the table, either in a final row that spans the entire table or under the last row in the table.

- Use reStructuredText markup to set the footnotes in the cells to which they apply. If numbers might be confusing (because maybe the text in the cells are numerical values), use symbols instead.

  - A footnote cited in a column header applies to the entire column.

  - A footnote cited in a table cell applies to the text in that cell. Use a cell-level footnote if the note applies to multiple cells in the table.

## Attribute or Parameter Tables in API documents

When creating attribute or parameter tables in API documents, use the following additional guidelines:

- For tables that describes JSON or XML attributes, write the first sentence of a description with an implied subject. For example, if the attribute is name, the description might be as follows: "Initial hostname of the server."

- For attributes or parameters, include the valid values and default value at the end of the description.

  - For request parameters, use the formats "Application accepts *n* or *n*." and "The default is *n*." For example, "Atlas accepts `true` or `false`." and "The default is `false`."

  - For response parameters, use the formats "Application returns *n* or *n*." and "The default is *n*." For example, "Atlas returns `true` or `false`." and "The default is `false`."

- If table descriptions or construction is complex, consider using a definition list or itemized list instead of a table.

- Avoid putting definition lists in tables.

## Examples

The following table explains the different parts of the preceding URL:

<table>
<tr>
<th id="Part%20of%20URL">
Part of URL

</th>
<th id="Explanation">
Explanation

</th>
</tr>
<tr>
<td headers="Part%20of%20URL">
`swift://`

</td>
<td headers="Explanation">
Prefix that passes file system requests to the Swift file system.

</td>
</tr>
<tr>
<td headers="Part%20of%20URL">
`acontainer`

</td>
<td headers="Explanation">
Name of the container in Swift that contains the objects to be accessed. Container names must conform to RFC952 restrictions for host names—that is, the characters A-Z, numbers 0-9, and the hyphen (-).

Nonconforming container names are inaccessible by swiftfs.

</td>
</tr>
<tr>
<td headers="Part%20of%20URL">
`aservice`

</td>
<td headers="Explanation">
User-friendly "service" name. A service name maps to a collection of configuration entries in the Hadoop core-site.xml file that specify where the container is located (for example, MongoDB-dfw).

</td>
</tr>
<tr>
<td headers="Part%20of%20URL">
`/path/to/files`

</td>
<td headers="Explanation">
Name of the object or objects in Swift to be referenced. Although Swift doesn't support paths, swiftfs attempts to interpret names that look like paths and behave appropriately. For example, an input path named `/path/to/*` would qualify all objects with names prefixed by `/path/to/`. Similarly, an output path of `/path/to/` would prefix the names of all newly created objects with `/path/to/`.

</td>
</tr>
</table>The following table provides the default values for the absolute limits:

**Absolute limits**

<table>
<tr>
<th id="Name">
Name

</th>
<th id="Description">
Description

</th>
<th id="Limit%20(default%20value)">
Limit (default value)

</th>
</tr>
<tr>
<td headers="Name">
Node count

</td>
<td headers="Description">
Maximum number of allowed data nodes

</td>
<td headers="Limit%20(default%20value)">
3

</td>
</tr>
<tr>
<td headers="Name">
Disk

</td>
<td headers="Description">
Maximum disk capacity across all data nodes, in gigabytes (GB)

</td>
<td headers="Limit%20(default%20value)">
4500

</td>
</tr>
<tr>
<td headers="Name">
RAM

</td>
<td headers="Description">
Maximum RAM across all data nodes, in gigabytes (GB)

</td>
<td headers="Limit%20(default%20value)">
23040

</td>
</tr>
<tr>
<td headers="Name">
VCPUs

</td>
<td headers="Description">
Maximum virtual CPUs across all data nodes

</td>
<td headers="Limit%20(default%20value)">
6

</td>
</tr>
</table>The following matrix indicates which upgrade scenarios are supported:

<table>
<tr>
<th id="Upgrade%20scenario">
Upgrade scenario

</th>
<th id="Supported">
Supported

</th>
<th id="Not%20supported">
Not supported

</th>
</tr>
<tr>
<td headers="Upgrade%20scenario">
4.2.0 to 4.2. *x*

</td>
<td headers="Supported">

</td>
<td headers="Not%20supported">
X

</td>
</tr>
<tr>
<td headers="Upgrade%20scenario">
4.1. *x* to 4.2.1

</td>
<td headers="Supported">
X

</td>
<td headers="Not%20supported">

</td>
</tr>
<tr>
<td headers="Upgrade%20scenario">
4.1. *x* to 4.2.0

</td>
<td headers="Supported">

</td>
<td headers="Not%20supported">
X

</td>
</tr>
<tr>
<td headers="Upgrade%20scenario">
4.1. *x* to 4.1. *x*

</td>
<td headers="Supported">
X

</td>
<td headers="Not%20supported">

</td>
</tr>
<tr>
<td headers="Upgrade%20scenario">
4.0.0 to 4.2. *x*

</td>
<td headers="Supported">

</td>
<td headers="Not%20supported">
X

</td>
</tr>
<tr>
<td headers="Upgrade%20scenario">
4.0.0 to 4.1. *x*

</td>
<td headers="Supported">
X

</td>
<td headers="Not%20supported">

</td>
</tr>
</table>The following chart compares these top content management systems (CMSs):

<table>
<tr>
<th id="">

</th>
<th id="Drupal">
Drupal

</th>
<th id="WordPress">
WordPress

</th>
</tr>
<tr>
<td headers="">
Homepage

</td>
<td headers="Drupal">
www.drupal.org

</td>
<td headers="WordPress">
www.wordpress.org

</td>
</tr>
<tr>
<td headers="">
About

</td>
<td headers="Drupal">
Drupal is a powerful, developer-friendly tool for building complex sites. Like most powerful tools, it requires some expertise and experience to operate.

</td>
<td headers="WordPress">
WordPress began as an innovative, easy-to-use blogging platform. With an ever-increasing repertoire of themes, plug-ins, and widgets, this CMS is also widely used for other website formats.

</td>
</tr>
<tr>
<td headers="">
Example sites

</td>
<td headers="Drupal">
Community Portal: Fast Company, Team Sugar

</td>
<td headers="WordPress">
Social Networking: PlayStation Blog

News Publishing: CNN Political Ticker

Education/Research: NASA Ames Research Center

News Publishing:The New York Observer

</td>
</tr>
<tr>
<td headers="">
Installation

</td>
<td headers="Drupal">
Drupal Installation Forum

</td>
<td headers="WordPress">
WordPress Installation Forum

</td>
</tr>
</table>