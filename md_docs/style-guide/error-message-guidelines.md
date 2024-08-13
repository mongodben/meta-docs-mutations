---
title: Error Message Guidelines
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/error-message-guidelines/
---

# Error Message Guidelines

Developers often ask a technical writer to edit error messages that they have written.

When you edit error messages, use the writing guidelines in this Style Guide as you would with other documentation that is curated by the Documentation team. Start with the information in the Quickstart.

This topic provides additional guidelines specific to reviewing messages for MongoDB development teams.

This information is also available in the Helix documentation.

## General Guidelines

When you review error messages, consider the following guidelines for them:

- Be courteous and do not blame the user.

- Use present tense to describe conditions that currently exist, or use past tense to describe a specific event that occurred in the past.

- Where possible, guide users with the imperative voice (for example, "Enter a valid email.") or the active voice (such as "The Control Panel is not responding.").

- Error messages must be short, accurate, complete, and helpful.

## Message Guidelines and Examples

Use the following guidelines when you review messages written for a control panel.

<table>
<tr>
<th id="Guideline">
Guideline

</th>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Guideline">
Use monospace font.

</td>
<td headers="Use">
When you right-click a SQL Server 2012 database and select **Properties**, the following error message appears:

`The user doesn't have permission to perform this action.`

</td>
<td headers="Don't%20use">
When you right-click a SQL Server 2012 database and select **Properties**, the following error message appears:

The user doesn't have permission to perform this action.

</td>
</tr>
<tr>
<td headers="Guideline">
Use complete sentences, when possible.

Include articles (a, an, the) to make the sentence complete. If possible, use active voice.

</td>
<td headers="Use">
The authentication token isn't valid.

</td>
<td headers="Don't%20use">
Invalid authentication token.

</td>
</tr>
<tr>
<td headers="Guideline">
Use more than one sentence if required for clarity.

Write brief and simple sentences that clearly state the problem. Separate the sentences with a period (or question mark, if applicable), but not with a semicolon.

</td>
<td headers="Use">
Provide a name for each domain. *null* isn't a valid domain name.

</td>
<td headers="Don't%20use">
You must provide a name for each domain and *null* isn't a valid name.

</td>
</tr>
<tr>
<td headers="Guideline">
Use proper punctuation. For guidelines, see Punctuation.

</td>
<td headers="Use">
`FED2-013: Token expiration cannot exceed seconds.`

</td>
<td headers="Don't%20use">
`FED2-013; Token expiration cannot exceed seconds.`

</td>
</tr>
<tr>
<td headers="Guideline">
Avoid using only uppercase letters.

Lines with excessive capitalization are hard to read. Use all uppercase letters only for words that require it, such as a keyword, a data type, or a specific table name that's displayed in all uppercase letters to a database user. For more information, see Capitalization.

</td>
<td headers="Use">
The requested image `$UUID` has automatic disk resizing disabled.

</td>
<td headers="Don't%20use">
THE REQUESTED IMAGE $UUID HAS AUTOMATIC DISK RESIZING DISABLED.

</td>
</tr>
<tr>
<td headers="Guideline">
When possible, include a recommendation, either a potential fix or a reference to a document for more information.

Messages should provide specific information about how the user should continue.

</td>
<td headers="Use">
The system is out of virtual IP addresses. Contact Support so they can allocate more virtual IP addresses.

The value -1.0 can't be accepted. Specify a positive integer value for the volume size.

</td>
<td headers="Don't%20use">
The system is out of virtual IP addresses.

The value -1.0 can't be accepted.

</td>
</tr>
<tr>
<td headers="Guideline">
Be specific and provide as much detailed information as possible.

</td>
<td headers="Use">
The live migration of instance 89a5e582-d3f3-4665-ate2-03c2114f0bib to host compute2 failed.

</td>
<td headers="Don't%20use">
Live migration failed.

</td>
</tr>
<tr>
<td headers="Guideline">
To represent an unspecified or generic number, use *n* as the variable and apply italics.

To represent an unspecified or unknown version number, use *x* for each digit and apply italics.

Using *n* and *x* consistently reduces the confusion users might experience with these conventions.

</td>
<td headers="Use">
The rate limit has been reached (*n* requests in 24 hours). Try again later.

</td>
<td headers="Don't%20use">
This option is available only for Ubuntu 12.*x*.

</td>
</tr>
<tr>
<td headers="Guideline">
Avoid blaming the user.

Rewrite messages that imply fault on the part of the user. Use passive voice when necessary.

</td>
<td headers="Use">
The request couldn't be understood by the server because of malformed syntax.

</td>
<td headers="Don't%20use">
You entered bad request syntax.

</td>
</tr>
<tr>
<td headers="Guideline">
Use positive statements.

Positive statements are easier to understand than negative statements.

</td>
<td headers="Use">
The given limit must be less than 50.

</td>
<td headers="Don't%20use">
The given limit can't be greater than 50.

</td>
</tr>
</table>

## Message Types

The following table includes the most common types of error messages:

<table>
<tr>
<th id="Type">
Type

</th>
<th id="Guidelines">
Guidelines

</th>
<th id="Example">
Example

</th>
</tr>
<tr>
<td headers="Type">
Error

</td>
<td headers="Guidelines">
Use error messages to inform the user that a problem in the system or application occurred. The user or system cannot continue the task until the problem is resolved.

</td>
<td headers="Example">
The file could not be found.

</td>
</tr>
<tr>
<td headers="Type">
Warning

</td>
<td headers="Guidelines">
Use warning messages to alert users about a condition that might cause problems in the future. The user can generally continue with their tasks, but those tasks might not be completed in a way that is expected.

</td>
<td headers="Example">
The service could not open all documents. Some documents were skipped.

</td>
</tr>
<tr>
<td headers="Type">
Information

</td>
<td headers="Guidelines">
Use information messages to provide information about normal conditions and operations.

</td>
<td headers="Example">
Updates are being processed.

</td>
</tr>
<tr>
<td headers="Type">
Confirmation

</td>
<td headers="Guidelines">
Use confirmation messages to ask the user to verify an action that the user or the system initiated. Use a confirmation prompt to ask the user for additional information to complete a step or to ask whether to save information for future use.

</td>
<td headers="Example">
Do you want to close this document without saving your changes?

</td>
</tr>
<tr>
<td headers="Type">
Success

</td>
<td headers="Guidelines">
Use success messages to tell the user that an action successfully completed.

</td>
<td headers="Example">
Server successfully deleted.

</td>
</tr>
</table>