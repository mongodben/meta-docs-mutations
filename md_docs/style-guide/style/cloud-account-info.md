---
title: API Placeholders
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/cloud-account-info/
---

# API Placeholders

When users learn how to use our API, they might copy the code and try to use it as given.

- In the API examples you provide, use variables for usernames, passwords, email addresses, API keys, and so on.

- Format the placeholder variables as `camelCase` and enclose them in curly braces (`{ }`).

- **API requests:** Enclose in a language-appropriate `code-block` directive. Use `.. code-block:: console` directive for `curl` examples.

- **API responses:** Enclose in a `.. code-block:: json` directive.

- Add the `:linenos:` option to the `.. code-block::` directive if the example is longer than 10 lines.

- Add the `:copyable: false` option the `.. code-block:: json` directive in the response. The user shouldn't try to copy the response.

## Best Practices for Placeholders

<table>
<tr>
<th id="Information">
Information

</th>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Information">
Username

</td>
<td headers="Use">
`yourUserName`

</td>
<td headers="Don't%20use">
robb4554

</td>
</tr>
<tr>
<td headers="Information">
Password

</td>
<td headers="Use">
`yourPassword`

</td>
<td headers="Don't%20use">
J$12345*

</td>
</tr>
<tr>
<td headers="Information">
Public API Key

</td>
<td headers="Use">
`{publicApiKey}`

</td>
<td headers="Don't%20use">
gzungyzc

</td>
</tr>
<tr>
<td headers="Information">
Private API key

</td>
<td headers="Use">
`{privateApiKey}`

</td>
<td headers="Don't%20use">
ac930128-c6dd-ae41-fe44-d985d008e703

</td>
</tr>
<tr>
<td headers="Information">
Project

</td>
<td headers="Use">
`{projectId}`

</td>
<td headers="Don't%20use">
0e18fec1d223b72f626d23f1

</td>
</tr>
<tr>
<td headers="Information">
Organization

</td>
<td headers="Use">
`{orgId}`

</td>
<td headers="Don't%20use">
6c2c15110ceb948cf4b8f38c

</td>
</tr>
</table>

## Best Practices for Simulated Placeholder Values

In example API operation requests and responses, in which we want users to see actual values from the system, use "real-looking" but imaginary values, use the following formats:

<table>
<tr>
<th id="Parameter">
Parameter

</th>
<th id="Value%20Format">
Value Format

</th>
<th id="Value%20Template">
Value Template

</th>
<th id="Example">
Example

</th>
</tr>
<tr>
<td headers="Parameter">
Public API Key

</td>
<td headers="Value%20Format">
8 lowercase ASCII-alphabetic characters

</td>
<td headers="Value%20Template">
XXXXXXXX

</td>
<td headers="Example">
gzungyzc

</td>
</tr>
<tr>
<td headers="Parameter">
Private API key

</td>
<td headers="Value%20Format">
16 lowercase hexdecimal digits formatted as 4-2-2-6 (32 characters)

</td>
<td headers="Value%20Template">
a1a1a1a1-a1a1-a1a1-a1a1-a1a1a1a1a1a1

</td>
<td headers="Example">
ac930128-c6dd-ae41-fe44-d985d008e703

</td>
</tr>
<tr>
<td headers="Parameter">
Project

</td>
<td headers="Value%20Format">
12 lowercase hexdecimal digits (24 characters)

</td>
<td headers="Value%20Template">
a1a1a1a1a1a1a1a1a1a1a1a1

</td>
<td headers="Example">
0e18fec1d223b72f626d23f1

</td>
</tr>
<tr>
<td headers="Parameter">
Organization

</td>
<td headers="Value%20Format">
12 lowercase hexdecimal digits (24 characters)

</td>
<td headers="Value%20Template">
a1a1a1a1a1a1a1a1a1a1a1a1

</td>
<td headers="Example">
6c2c15110ceb948cf4b8f38c

</td>
</tr>
</table>Use a random number generator to create the placeholders. One example would be the Generate Random Hex tool.

Never include or show actual writer or user account credentials in code examples or screenshots.