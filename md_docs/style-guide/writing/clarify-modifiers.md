---
title: Clarify Ambiguous Modifiers
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/clarify-modifiers/
---

# Clarify Ambiguous Modifiers

Modifiers that can be misinterpreted as being associated with a word other than the one intended, or with no particular word at all, are called *misplaced* or *dangling modifiers*.

In general, move the modifier closer to the noun or phrase it modifies to increase clarity.

## Misplaced Modifiers

Simple adverbs used to convey limits (such as *almost*, *hardly*, *nearly*, *just*, *only*, or *merely*) can change the meaning of your writing depending on their placement in the sentence. Ensure that these modifiers are placed correctly so that they convey your intended meaning.

In the following examples, the placement of *only* greatly affects the meaning of the sentence:

<table>
<tr>
<th id="Example">
Example

</th>
<th id="Meaning">
Meaning

</th>
</tr>
<tr>
<td headers="Example">
The `db.collection.createIndex` method **only** creates an index if an index of the same specification does not already exist.

</td>
<td headers="Meaning">
The `db.collection.createIndex` method could create other things, but if an index of the same specification does not already exist, it will create an index. If an index of the same specification already exists, the method could do something else.

</td>
</tr>
<tr>
<td headers="Example">
The `db.collection.createIndex` method creates an index **only** if an index of the same specification does not already exist.

</td>
<td headers="Meaning">
The `db.collection.createIndex` method can create an index when an index of the same specification does not already exist. If an index of the same specification exists, it will not create an index.

</td>
</tr>
<tr>
<td headers="Example">
**Only** the `db.collection.createIndex` method creates an index if an index of the same specification does not already exist.

</td>
<td headers="Meaning">
No other method can create an index if an index of the same specification does not already exist. Another method could create an index if an index of the same specification exists.

</td>
</tr>
</table>The placement of phrases or clauses can tweak your meaning or make things ambiguous as well:

<table>
<tr>
<th id="Use">
Use

</th>
<th id="Avoid">
Avoid

</th>
<th id="Avoid%20Meaning">
Avoid Meaning

</th>
</tr>
<tr>
<td headers="Use">
On Monday, MongoDB announced that they would release a new feature. *or* MongoDB announced that they would release a new feature on Monday.

</td>
<td headers="Avoid">
MongoDB announced on Monday they would release a new feature.

</td>
<td headers="Avoid%20Meaning">
*Does this mean MongoDB made an announcement on Monday? Or that a new feature would be released on Monday?*

</td>
</tr>
<tr>
<td headers="Use">
You must increase the storage size of the instance when it's at full capacity.

</td>
<td headers="Avoid">
When at full capacity, you must increase the storage size of the instance.

</td>
<td headers="Avoid%20Meaning">
*This means the user is at full capacity, not the instance.*

</td>
</tr>
</table>

## Dangling Modifiers

Modifier clauses at the beginning or end of a sentence should modify the subject of the main clause. When the subject is missing or the clause modifies another object in the sentence, the clause is called a dangling modifier.

<table>
<tr>
<th id="Use">
Use

</th>
<th id="Avoid">
Avoid

</th>
<th id="Avoid%20Meaning">
Avoid Meaning

</th>
</tr>
<tr>
<td headers="Use">
When you log in to Atlas, your clusters are displayed.

</td>
<td headers="Avoid">
Logging in to Atlas, your clusters display.

</td>
<td headers="Avoid%20Meaning">
This sentence means that your clusters are logging in, not the user.

</td>
</tr>
<tr>
<td headers="Use">
The replica set elects a new primary after you force an election.

</td>
<td headers="Avoid">
The replica set elects a new primary after forcing an election.

</td>
<td headers="Avoid%20Meaning">
This sentence means that the replica set itself forced an election, not the user.

</td>
</tr>
</table>