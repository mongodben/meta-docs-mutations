---
title: Clarify Pronouns and Antecedents
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/use-pronouns-carefully/
---

# Clarify Pronouns and Antecedents

Pronouns are useful, but you must make sure that their antecedents (the words that the pronouns replace) are clear, and that the pronouns don’t cause vagueness and ambiguity.

The following pronouns often cause problems, so use them carefully: *it*, *this*, *there*, and *that*.

## It

Make sure that the antecedent of *it* is clear. If multiple singular nouns precede *it*, any of them could be the antecedent.

Avoid using *it is* (or *it's*) to begin a sentence. Such a construction hides the real subject of the sentence.

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
You can store the value and use it again later.

</td>
<td headers="Avoid">
The product stores the value in the configuration file. You can use it again later. (The antecedent of it could be the product, the value, or the file.)

</td>
</tr>
<tr>
<td headers="Use">
You must close all open windows before you run the script.

</td>
<td headers="Avoid">
It is important that you close all open windows before you run the script.

</td>
</tr>
<tr>
<td headers="Use">
If you use a resume token, Atlas attempts to resume the trigger’s underlying change stream at the event immediately following the last change event the trigger processed.

</td>
<td headers="Avoid">
If you use a resume token, Atlas attempts to resume the trigger’s underlying change stream at the event immediately following the last change event it processed. (The antecedent of it could be Atlas or the trigger.)

</td>
</tr>
</table>

## This

Avoid beginning a sentence with the pronoun *this*, unless you follow *this* with a noun to clarify its meaning.

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
This option causes an error when you run the program.

</td>
<td headers="Avoid">
This causes an error when you run the program.

</td>
</tr>
</table>

## There

Avoid using *there is* and *there are* as the subject of a sentence or clause. Using *there* shifts the focus away from the real subject and often uses unnecessary words.

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
This option has no parameter.

*or*

No parameter exists for this option.

</td>
<td headers="Avoid">
There is no parameter for this option.

</td>
</tr>
<tr>
<td headers="Use">
When errors occur in the script, the product writes information to the message log.

</td>
<td headers="Avoid">
When there are errors in the script, the product writes information to the message log.

</td>
</tr>
<tr>
<td headers="Use">
The FTP service supports resumable uploading. If a connection fails during an upload, you don't need to restart the upload from the beginning.

</td>
<td headers="Avoid">
The FTP service supports resumable uploading. This means that if there is a connection failure during an upload, it doesn't have to be started from the beginning.

</td>
</tr>
</table>

## That

Although you should use *that* as a relative pronoun (see Use *that*, *which*, and *such as* Correctly), avoid using it as a demonstrative pronoun (which stands in for or points to a noun). Use it as an adjective and follow it with a noun.

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
Use that method.

</td>
<td headers="Avoid">
That is the method to use.

</td>
</tr>
<tr>
<td headers="Use">
You can also edit or delete your `CNAME` by managing your DNS in your existing tool.

</td>
<td headers="Avoid">
If you want to edit or delete your `CNAME`, you can also do that by managing your DNS in your existing tool.

</td>
</tr>
</table>