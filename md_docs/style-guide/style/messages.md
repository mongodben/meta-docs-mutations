---
title: Messages
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/messages/
---

# Messages

If you help write the message text for a product or you suggest edits to message text, use the guidelines in this topic.

Change message text *only* at the request of (or as a suggestion to) the developer. When citing message text in a document, cite the text that the user sees in the product.

<table>
<tr>
<th id="Guideline">
Guideline

</th>
<th id="Example">
Example

</th>
<th id="Comments">
Comments

</th>
</tr>
<tr>
<td headers="Guideline">
Use complete sentences, when possible.

</td>
<td headers="Example">
*Use:*

The authentication token isn't valid.

*Avoid:*

Invalid authentication token

</td>
<td headers="Comments">
Include articles (*a*, *an*, *the*) to make the sentence complete. If possible, use active voice.

Message text that serves as a heading or label (such as `Elapsed:hh:mm:ss`, which indicates elapsed time) is acceptable as a fragment.

</td>
</tr>
<tr>
<td headers="Guideline">
Use more than one sentence if required for clarity.

</td>
<td headers="Example">
You must provide a name for each domain. null isn't a valid domain name.

</td>
<td headers="Comments">
Write brief and simple sentences that clearly state the problem. Separate the sentences with a period (or question mark, if applicable), not with a semicolon.

</td>
</tr>
<tr>
<td headers="Guideline">
Avoid using only uppercase letters.

</td>
<td headers="Example">
*Use:*

The requested image $UUID has automatic disk resizing disabled.

*Avoid:*

THE REQUESTED IMAGE $UUID HAS AUTOMATIC DISK RESIZING DISABLED.

</td>
<td headers="Comments">
Lines with excessive capitalization are hard to read. Use all uppercase letters only for words that require it, such as a keyword, a data type, or a specific table name that's displayed in all uppercase letters to a database user.

</td>
</tr>
<tr>
<td headers="Guideline">
When possible, include a recommendation, either a potential fix or a reference to a document for more information.

</td>
<td headers="Example">
The system is out of virtual IP addresses. Contact Support so they can allocate more virtual IP addresses.

The value -1.0 can't be accepted. Specify a positive integer value for the volume size.

</td>
<td headers="Comments">
Messages should provide specific information about how the user should continue.

</td>
</tr>
<tr>
<td headers="Guideline">
Be specific.

</td>
<td headers="Example">
*Use:*

The live migration of instance 89a5e582-d3f3-4665-ate2-03c2114f0bib to host compute2 failed.

*Avoid:*

Live migration failed.

</td>
<td headers="Comments">
Messages should provide as much detailed information as possible.

</td>
</tr>
<tr>
<td headers="Guideline">
Use *n* to represent an unspecified or generic number. Use *x* to represent an unknown version number.

</td>
<td headers="Example">
The rate limit has been reached (*n* requests in 24 hours). Please try again later.

This option is available only for Ubuntu 12. *x*.

</td>
<td headers="Comments">
None

</td>
</tr>
<tr>
<td headers="Guideline">
Avoid blaming the user.

</td>
<td headers="Example">
*Use:*

The request couldn't be understood by the server because of malformed syntax.

*Avoid:*

You entered bad request syntax.

</td>
<td headers="Comments">
Rewrite messages that imply fault on the part of the user. Use passive voice when necessary.

</td>
</tr>
<tr>
<td headers="Guideline">
When possible, use positive statements.

</td>
<td headers="Example">
*Use:*

The given limit must be positive and must be less than 50.

*Avoid:*

The given limit can't be negative and can't be greater than 50.

</td>
<td headers="Comments">
Positive statements are easier to understand than negative statements.

</td>
</tr>
</table>