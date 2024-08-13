---
title: Use Active Voice
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/use-active-voice/
---

# Use Active Voice

## Why Use Active Voice?

- *Active voice* makes the *performer* of the action (usually the reader or user) the subject of the sentence.

- *Passive voice* makes the *recipient* of the action (not the performer) the subject of the sentence.

When compared to passive-voice sentences, active-voice sentences are:

- more engaging

- less complicated

- less wordy

- easier to understand

With active voice, you can distinguish the actions and responses of the user from those of the technology.

Beginning users look for specific calls to action in procedures. Active voice makes this clear.

Consider if you write a step that reads "The service can be restarted".

As written, this sentence reads as a *consideration* or a *possibility*, not an *instruction*. If the user skips this step due to this confusion, the rest of the tutorial might fail.

If you write "Restart the service", you remove all doubt. It saves the tutorial. This also clarifies that the user restarts the service.

In some systems, a service might restart itself after a failure. Active voice distinguishes between situations when a service acts and a user needs to act. "Restart the server" leaves no confusion over who performs the action: the user.

<table>
<tr>
<th id="Use%20(active)">
Use (active)

</th>
<th id="Avoid%20(passive)">
Avoid (passive)

</th>
</tr>
<tr>
<td headers="Use%20(active)">
After you install the software, start the computer.

</td>
<td headers="Avoid%20(passive)">
After the software has been installed, the computer can be started.

</td>
</tr>
<tr>
<td headers="Use%20(active)">
Click OK to save the configuration.

</td>
<td headers="Avoid%20(passive)">
The configuration is saved when the OK button is clicked.

</td>
</tr>
<tr>
<td headers="Use%20(active)">
Create a server.

</td>
<td headers="Avoid%20(passive)">
A server is created by you.

</td>
</tr>
<tr>
<td headers="Use%20(active)">
MongoDB products and services solve your business problems.

</td>
<td headers="Avoid%20(passive)">
Your business problems are solved by MongoDB products and services.

</td>
</tr>
</table>

## When Do You Use Passive Voice?

You can use passive voice when using active voice:

- Sounds like you're blaming the user. For example, you can use passive voice in an error message or troubleshooting content when the active subject is the user.

- Makes the sentence wordy or awkward.

- Would emphasize the performer when you don't know the performer of action or you want to de-emphasize the performer in favor the object on which the action is performed.

<table>
<tr>
<th id="Acceptable%20(passive)">
Acceptable (passive)

</th>
<th id="Avoid%20(active)">
Avoid (active)

</th>
<th id="Why?">
Why?

</th>
</tr>
<tr>
<td headers="Acceptable%20(passive)">
If the build fails, the flavor might have been omitted.

</td>
<td headers="Avoid%20(active)">
If the build fails, you probably omitted the flavor.

</td>
<td headers="Why?">
The active voice blames the user.

</td>
</tr>
<tr>
<td headers="Acceptable%20(passive)">
A flag was set incorrectly.

</td>
<td headers="Avoid%20(active)">
You set the flag incorrectly.

</td>
<td headers="Why?">
The active voice blames the user.

</td>
</tr>
<tr>
<td headers="Acceptable%20(passive)">
Account owners can't be assigned additional roles, and their access can't be restricted.

</td>
<td headers="Avoid%20(active)">
Administrators can't assign account owners additional roles, and they can't restrict the access of account owners.

</td>
<td headers="Why?">
In this context, the object, account owners, is more important than the actor, administrators.

</td>
</tr>
</table>