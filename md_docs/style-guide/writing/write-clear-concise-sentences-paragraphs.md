---
title: Write Clear and Concise Sentences and Paragraphs
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/write-clear-concise-sentences-paragraphs/
---

# Write Clear and Concise Sentences and Paragraphs

Users can understand wordy and complex writing. They can wade through walls of text, but we shouldn't force them to do that. Use the following guidelines to clarify and condense sentences and paragraphs.

## Use a Consistent Sentence Structure

- As often as possible, use the sentence structure *subject*-*verb*-*object*.

- Use simple declarative sentences for descriptions.

- Use simple imperative sentences for instructions.

- Sentences that describe a condition should always begin with the conditional clause, so that the user can skip the section if the condition does not apply to them.

- Don't make users backtrack to understand a sentence. If they can't understand the beginning of the sentence without reading the end, rewrite the sentence.

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
Atlas truncate the value only when it's stored as an integer.

</td>
<td headers="Avoid">
Only when stored in an integer variable is the value truncated.

</td>
</tr>
<tr>
<td headers="Use">
To bake a cake, follow these steps.

</td>
<td headers="Avoid">
Take a look at the following procedure below to bake a simple cake.

</td>
</tr>
<tr>
<td headers="Use">
If you must monitor clients from the host, you can configure your settings in the directory.

</td>
<td headers="Avoid">
You can configure your settings in the directory if you must monitor clients from the host.

</td>
</tr>
<tr>
<td headers="Use">
Many users struggle to parse dense content.

</td>
<td headers="Avoid">
Gathering the data necessary to parse dense content effectively is a task struggled with by many users.

</td>
</tr>
</table>

## Restrict Sentence Length

A well-written long sentence may be hard to follow and understand.

- Try to limit sentences to no more than 20-25 words. Limit to less than 20 words if possible.

- If you must write a longer sentence: - Use more than one clause. - Clarify the relationship between the clauses.

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
After you choose a cloud provider, Atlas fetches a list of the regions where the provider can host a cluster. Atlas displays the default cluster tier with its memory and storage parameters.

</td>
<td headers="Avoid">
After you choose a cloud provider, Atlas fetches a list of the regions where the cloud provider can host a cluster, along with the cluster tier and the memory and storage parameters for that tier.

</td>
</tr>
<tr>
<td headers="Use">
Select whether to overwrite files with the same name or to restore files to their original folders. Click Next.

</td>
<td headers="Avoid">
Click the check boxes to confirm whether you would like to Overwrite files with the same name or restore the files to their original folders and then click the Next button.

</td>
</tr>
</table>
### Limit Using *Be* as the Main Verb

Pay special attention if a form of be is the main verb in the sentence. Forms of *be* include:

- *be*

- *is*

- *am*

- *are*

- *was*

- *were*

- *being*

- *been*

Look for a "hidden" verb in the element following the *be*‐verb.

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
This report analyzes the problem.

</td>
<td headers="Avoid">
This report is an analysis of the problem.

</td>
</tr>
</table>

### Avoid Expletive Structures

An expletive sentence begins with *It* or *There* and followed by a form of *be*. Consider another noun and verb following the expletive.

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
We need to solve this problem.

</td>
<td headers="Avoid">
It is necessary for us to find a solution to this problem.

</td>
</tr>
<tr>
<td headers="Use">
Cloud backup has three benefits over legacy backup.

</td>
<td headers="Avoid">
There are three benefits to the cloud backup compared to the legacy backup.

</td>
</tr>
</table>

### Avoid Nominalizations

A *nominalization* is a noun derived from a verb. These words often end in -ance, -ence, -ion, or -ment. Identify the verb at the root of the nominalization and use it instead.

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
The modal recommends upgrading to new software.

</td>
<td headers="Avoid">
The modal contains a recommendation that the user upgrade to new software.

</td>
</tr>
<tr>
<td headers="Use">
It benefits users to have this information.

</td>
<td headers="Avoid">
It would be beneficial to the users if they had this information.

</td>
</tr>
</table>

## Use the Necessary Words

Business and technical writing isn't creative writing.

- Limit yourself to the words necessary to convey the meaning.

- Remove anything extraneous.

  - Are you using adverbs (modifiers ending in *-ly*)? You can remove most adverbs without changing the meaning.

  - Are you using adjectives? Remove them if they aren't necessary to the meaning. Some features have adjectives in their names. Don't remove those.

  - Can you shorten prepositional phrases?

  - Are you using phrases that don't clarify the content?

- Include all necessary words that clarify the meaning of a sentence.

  - Include all necessary articles (*a*, *an*, *the*), prepositions, connectors, and other syntactic cues, such as those described in Clarify Gerunds and Participles, Use *that*, *which*, and *such as* Correctly, and Clarify Pronouns and Antecedents.

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
Use the product to create temporary URLs for your files. You can share these URLs with other people.

</td>
<td headers="Avoid">
A great feature implemented by the product is the ability to generate temporary URLs for files and share them with other people.

</td>
</tr>
<tr>
<td headers="Use">
Use the Control Panel to create servers easily and quickly.

</td>
<td headers="Avoid">
The well-designed Control Panel is your passport to creating servers in an easy, fun way right away.

</td>
</tr>
<tr>
<td headers="Use">
Many businesses want one system to collaborate, manage content, and aid in decisions. SharePoint serves as the logical choice for these needs.

</td>
<td headers="Avoid">
The flexibility, extensibility, rich feature set and ease-of-use offered by SharePoint make it the logical choice for many businesses when it comes to their Collaboration, Content Management and Business Intelligence needs.

</td>
</tr>
<tr>
<td headers="Use">
In an environment where you run MongoDB, you can use Ops Manager to monitor and audit your backup and recovery activities across the MongoDB clusters.

</td>
<td headers="Avoid">
In an environment where MongoDB is installed and running on one or more hosts, Ops Manager enables you to monitor your backup and recovery activities and audit your backup and recovery practices from an enterprise-wide perspective.

</td>
</tr>
<tr>
<td headers="Use">
Empty the file.

</td>
<td headers="Avoid">
Empty file.

</td>
</tr>
<tr>
<td headers="Use">
The Label option isn't supported for this file format.

</td>
<td headers="Avoid">
Label option not supported for file format.

</td>
</tr>
</table>

## Create Short Paragraphs

Short paragraphs are easier to scan and understand than longer ones. Use the following guidelines for paragraphs:

- Cover only one idea in each paragraph.

- Limit paragraphs to four to five sentences.

- Avoid having one-sentence paragraphs.

- Use connective or transitional words to ensure flow within and between paragraphs.

- When listing three or more items, use a bullet list instead of embedding the items in a paragraph.

The following examples show how you can break up a long paragraph. Use a list so the user can scan the text.

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
From the Job Scheduler window, you can perform the following actions:

- Run a generated script immediately.

- Schedule a generated script to run at a later time.

- Track the execution of submitted jobs.

- Manage jobs in the job queue.

</td>
<td headers="Avoid">
From the Job Scheduler page, you can run a generated script immediately, schedule a generated script to run at a later time, track the execution of submitted jobs, and manage jobs in the job queue.

</td>
</tr>
<tr>
<td headers="Use">
Within the Cloud Storage App for Microsoft SharePoint, you can delete a single file or multiple files from a container:

- To delete a single file, click the delete icon to the right of the file's name.

- To delete multiple files at one time, select the cloud icon to the left of each file's name and then click **Delete Selected**. Rows that you select for deletion are highlighted with a dark gray background.

When you delete a file, it's permanently removed from the Cloud Files container.

</td>
<td headers="Avoid">
Within the Cloud Storage App for Microsoft SharePoint, you can delete a single file or multiple files from a container. You can delete a single file by clicking the delete icon to the right of the file's name. You can delete multiple files at one time by selecting the cloud icon to the left of each file's name and then clicking Delete Selected. Rows that you select for deletion are highlighted with a dark gray background. When you delete a file, it's permanently removed from the Cloud Files container.

</td>
</tr>
</table>For style guidelines for lists, see Lists.