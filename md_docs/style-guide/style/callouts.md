---
title: Callouts and Admonitions
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/callouts/
---

# Callouts and Admonitions

Callouts or admonitions emphasize important or helpful information. To avoid clutter on the page and to preserve visual impact, use callouts sparingly.

## Callout Types

You can use the following callouts:

<table>
<tr>
<th id="Callout%20Type">
Callout Type

</th>
<th id="Description">
Description

</th>
<th id="Directive">
Directive

</th>
</tr>
<tr>
<td headers="Callout%20Type">
Tip

</td>
<td headers="Description">
Provides useful information that might improve product performance or make procedures easier to follow. Tips provide the following benefits:

- Help users learn techniques or procedures

- Show alternative ways of doing something

- Provide shortcuts

- Provide helpful (but not essential) information

</td>
<td headers="Directive">
`.. tip:: <title>`

</td>
</tr>
<tr>
<td headers="Callout%20Type">
Note

</td>
<td headers="Description">
Provides information that emphasizes or supplements information in the text. A note can provide information that applies only in certain cases.

</td>
<td headers="Directive">
`.. note:: <title>`

</td>
</tr>
<tr>
<td headers="Callout%20Type">
Important

</td>
<td headers="Description">
Presents an important or essential point. As a rule, users must pay attention to important callouts to complete a task or understand a topic.

</td>
<td headers="Directive">
`.. important:: <title>`

</td>
</tr>
<tr>
<td headers="Callout%20Type">
Warning

</td>
<td headers="Description">
Alerts users to potential hazards or highlights critical information. Use a warning for situations in which users could lose data, compromise data integrity, or disrupt operations if they don't follow instructions carefully.

</td>
<td headers="Directive">
`.. warning:: <title>`

</td>
</tr>
<tr>
<td headers="Callout%20Type">
Example

</td>
<td headers="Description">
Presents a scenario that illustrates or demonstrates a concept in the text.

</td>
<td headers="Directive">
`.. example:: <title>`

</td>
</tr>
<tr>
<td headers="Callout%20Type">
See

</td>
<td headers="Description">
Provides a link to a topic or section directly related to the preceding text. You might use `see` to link to content with necessary procedures, definitions, or deployment considerations and impacts.

</td>
<td headers="Directive">
`.. see::`

</td>
</tr>
<tr>
<td headers="Callout%20Type">
See also

</td>
<td headers="Description">
Provides a link to topics or sections that are generally related to or provide useful context for the preceding text. You might use `seealso` to link to content that provides background information, deeper context, or common related tasks.

</td>
<td headers="Directive">
`.. seealso::`

</td>
</tr>
</table>

## Callout Guidelines

When creating callouts, use the following guidelines:

- Use the callout type to convey the kind of information you want to communicate. Don't rely on color to convey intensity.

- Use the correct reStructuredText directive to create the callout. Don't attempt to create callouts using boldface, headings, or custom CSS (Cascading Style Sheets).

- Don't stack multiple callouts directly after one another, as these can distract users. To avoid stacking callouts, group supplemental information from callouts into a dedicated section.

- If possible, don't use callouts in tables and option lists Callouts reduce the scannability of tables and options lists.

- Avoid nesting callouts inside tables and other elements.

- Avoid nesting code blocks inside callouts.

- Place a callout as close as possible to the information that it emphasizes or clarifies.

- Avoid stacking callouts of the same type. For example, avoid adding one labeled note directly after another labeled note. Instead, use a single callout that contains separate paragraphs or an unordered list.

The following callouts might appear in existing documentation but are deprecated. Don't use these callouts in new content:

- `.. admonition::`

- `.. caution::`

- `.. danger::`

- `.. topic::`