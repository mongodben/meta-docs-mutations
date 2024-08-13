---
title: Use Present Tense
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/use-present-tense/
---

# Use Present Tense

Users read content to learn how to perform tasks or to gather information. These activities occur in the users' present time. This makes the present tense appropriate in most cases. The present tense implies that users should take action now. Sentences that use the present tense are easier to read than sentences that use past or future tense.

The future tense may imply a sense of uncertainty. (We can't guarantee a future action, regardless of expectation!) Use future tense to emphasize that something occurs later from the users' perspective.

The past tense may be used when you need to refer to a past event or, more often, an earlier software release. Limit references to earlier versions to the immediate prior release. If a user wants to learn about something earlier than that can refer to an earlier version of the documentation.

To easily find and remove instances of future tense, search for *will*.

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
The product *prompts* you to verify the deletion.

</td>
<td headers="Avoid">
The product *will prompt* you to verify the deletion.

</td>
</tr>
<tr>
<td headers="Use">
After you log in, MongoDB Atlas *begins* the verification process.

</td>
<td headers="Avoid">
After you log in, MongoDB Atlas *will then begin* the verification process.

</td>
</tr>
<tr>
<td headers="Use">
MongoDB Atlas *uses* your GCP Service Account Key to encrypt and decrypt your MongoDB master keys.

</td>
<td headers="Avoid">
MongoDB Atlas *will use* your GCP Service Account Key to encrypt and decrypt your MongoDB master keys.

</td>
</tr>
<tr>
<td headers="Use">
Any customer with an Atlas account *can provision* multiple MongoDB database instances.

</td>
<td headers="Avoid">
Any customer with an Atlas account *will be able to provision* multiple MongoDB database instances.

</td>
</tr>
<tr>
<td headers="Use">
The migrations will begin in June 2017 and continue through July 2017.

</td>
<td headers="Avoid">
Not applicable. Future tense is appropriate in this example.

</td>
</tr>
</table>