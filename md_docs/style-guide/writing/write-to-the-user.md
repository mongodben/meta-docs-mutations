---
title: Use Second Person and Imperative Mood
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/write-to-the-user/
---

# Use Second Person and Imperative Mood

## Write to the User

Users are more engaged with content when it talks to them directly. Use *second person* to talk to users directly, addressing the user as *you*. Second person promotes a friendly tone.

- Use second person with the imperative mood (in which the subject *you* is understood) and active voice to eliminate wordiness and confusion about who or what initiates an action, especially in procedural steps.

  All of the guidelines in this list, and most of the guidelines in the style guide, use second person, imperative mood, and active voice.

- Use second person to avoid the use of gender-specific, third-person pronouns:

  - *he*

  - *she*

  - *his*

  - *hers*

  - *him*

  - *her*

  - *himself*

  - *herself*

  If you must use third person, use the pronouns:

  - *they*

  - *them*

  - *their*

  - *themselves*

  Verify that the pronoun's antecedent is plural.

  Using third person rarely makes sense. Second person should address most reference and instructional material.

- Use first-person plural pronouns (*we*, *our*) judiciously. These pronouns emphasize the writer or MongoDB rather than the user. Before using first-person pronouns, consider second person or imperative mood instead.

  - Use *we recommend* rather than *it's recommended* or *MongoDB recommends*. Limit how often you state recommendations. This expresses an opinion on behalf of MongoDB. Make sure that the engineering team or TSE team has expressed this opinion before stating anything as a recommendation. You should be prepared to defend any recommendations you publish with a ticket number from engineering or the TSE organization.

  - You can use *we* in the place of *MongoDB* if necessary.

- Use the first-person singular pronoun *I* only in the question part of FAQs.

- Avoid switching person (point of view) in the same document.

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
To create a cluster, specify a name and tier. (imperative)

To create a cluster, you specify a name and tier.

</td>
<td headers="Avoid">
Creating a cluster involves specifying a name and tier.

To create a cluster, the user specifies a name and tier.

</td>
</tr>
<tr>
<td headers="Use">
Click Yes to accept the license agreement.

</td>
<td headers="Avoid">
The license agreement is accepted when the user clicks Yes.

</td>
</tr>
<tr>
<td headers="Use">
We offer you a comprehensive portfolio of hosting options.

</td>
<td headers="Avoid">
MongoDB offers a comprehensive portfolio of hosting options for the enterprise buyer.

</td>
</tr>
<tr>
<td headers="Use">
Providing you a fantastic experience sets MongoDB apart. We are here to help, 24×7×365.

</td>
<td headers="Avoid">
MongoDB is here to help customers.

</td>
</tr>
<tr>
<td headers="Use">
Cloud Backup uses block-level deduplication, which means that only those parts of a file that have changed are saved.

</td>
<td headers="Avoid">
Cloud Backup uses block-level deduplication, which means we save only those parts of a file that have changed.

</td>
</tr>
<tr>
<td headers="Use">
I want to update everyone about the current status of the project and our future plans. (from a blog post)

</td>
<td headers="Avoid">
This post describes the current status of the project and future plans.

</td>
</tr>
</table>

## Avoid the Subjunctive Mood

The subjunctive mood expresses doubt. *That doesn’t engender trust from readers about our content!* Avoid words that imply uncertainty:

- should

- could

- would

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
The logs download as a `.CSV` file.

</td>
<td headers="Avoid">
The logs should download as a `.CSV` file.

</td>
</tr>
<tr>
<td headers="Use">
If you install the MongoDB Agent, you can manage your deployment with Automation.

</td>
<td headers="Avoid">
If you were to install the MongoDB agent, you could manage your deployment with Automation.

</td>
</tr>
</table>Readers expect documentation to be authoritative. If you don't know which one of two options is correct, research or ask engineering to find the exact answer. Document what you discover. Don't use language that gives the user more questions.

Production notes and other similar resources where we recommend best practices configuration settings for use with MongoDB offerings.

You should set your `vm.swappiness` to `1` if possible.

This language presents an ideal configuration, but does not *mandate* it.