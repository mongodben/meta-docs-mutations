---
title: Links and Cross-References
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/links-and-cross-references/
---

# Links and Cross-References

Documentation writers use links to direct users to related material outside of the current page or section. Links may be:

- Inline textual references to different sections. For example:

  "Partial indexes include more details about indexed documents compared to Sparse Indexes."

- Explicit references to different sections. For example:

  "To learn more about aggregation pipelines, see:

  - Expression Operators

  - Aggregation Stages

  - Practical MongoDB Aggregations"

- Explicit hyperlinks to specific URLs. For example, a link to a GitHub repository.

## Best Practices

Use the following guidelines to create clear and specific links and cross-references.

### Link with Care

Before you link to a separate page or section, consider whether that link actually aids user understanding. To minimize reader disruption, aim to keep users on the page they're currently reading as much as possible. If you are considering adding a link, see if the content would be better served by providing a brief definition or key concept on the page the reader is currently reading, rather than making the user do additional navigation on their own.

Be aware that providing a brief definition or attempting to explain a concept on the current page may introduce maintenance issues. If the behavior of the topic we're describing changes, it may become more difficult to track down each place that topic is mentioned and know what needs to be updated. When possible, use an include to single-source content and reduce future maintenance.

### Consider Link Placement

Generally, an explicit reference at the end of a page or section is less disruptive than an inline textual reference, especially when there are several inline references in succession. If you introduce a few concepts you'd like to provide links to, consider grouping links to concepts into either:

- A "Learn More" section with a consolidated list of links.

- A `..seealso` directive at the end of the section.

By using one of these approaches, users who just want to complete a task aren't distracted by additional links, and users who want to learn more about MongoDB concepts can click through and explore the linked content.

### Avoid Inline References in Tutorials

Avoid adding inline textual references in tutorials or stepped procedures. If users follow inline references while in the middle of a procedure, they might have difficulty navigating back and reorienting themselves. Inline textual references may be appropriate for more reference-heavy pages.

### Minimize Repeated Links

- Don't link to the same target multiple times in the same section. You may link to the same target multiple times on the same page, but think carefully about whether it's absolutely necessary. For example, if a page is particularly long and contains many sections, then it might help to link to a target an additional time or two. Users might immediately navigate to a section far down on a page and miss the initial reference.

- If you add repeated links, use the same style for each link. Consider whether a plaintext link or a monospace link is appropriate. Plaintext links might be less visually distracting than monospace links, which have a surrounding block.

### Make Link Text Clear

Strive to be clear about where exactly a link will take a reader. Follow these guidelines for link text to ensure readers know the purpose of a link and where it will take them:

- Use descriptive text indicating where the URL will take the reader.

- Avoid jargon in link text. Using technical terms as needed, such as the name of an operator or method, is appropriate.

- Use normal English words as opposed to URLs.

- If a link will take a user away from the MongoDB documentation, such as to GitHub or Wikipedia, make the target site clear in the link text.

- Avoid "Click here." It's bad for search engine optimization, screen readers, and doesn't adequately describe the target.

Link text should begin with the purpose of the cross-reference. For example:

- "To learn more, see..."

- "To see examples..."

The linked text should correspond to the title of the page or section you are linking to. For example, consider the following sentence which provides a cross-reference:

To learn more, see the guide on Finding Multiple Documents in the Node.js Driver Documentation.

The linked text should correspond to the title of the guide. In this example, the title of the guide is "Finding Multiple Documents". The complete link sentence should look like this:

To learn more, see the guide on Finding Multiple Documents in the Node.js Driver Documentation.

### Use MongoDB-Domain Links When Possible

Link to the MongoDB domain whenever possible instead of directing users to external domains. Some topics described in our documentation are also covered by other products' documentation, external tutorials, or Wikipedia. By keeping users in the MongoDB domain, we ensure that we are in full control of the content presented, and maintain trust with users.

Directing users outside of the MongoDB domain is acceptable when it is critical to provide additional context on a topic and we don't have sufficient context in our documentation to cover user needs.

### Use `:ref:` Links Instead of `:doc:` Links

When linking to content within the MongoDB documentation, use `:ref:` links instead of `:doc:` links. `:ref:` links make maintenance easier in the event that a section is refactored or consolidated into a new page because we can simply bring the reference along with the paragraph or section we're pointing to. When using `:doc:` links, a refactor can potentially break links if the page is renamed or removed.

## Link and Cross-Reference Examples

All MongoDB URLs should have a trailing slash to match standards for canonical URLs used for SEO purposes.

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
To learn more about storage engines, see Storage in the MongoDB manual.

</td>
<td headers="Avoid">
See Storage for more information on storage engines.

</td>
</tr>
<tr>
<td headers="Use">
The snapshot retention policy is described in Backup Scheduling, Retention, and On-Demand Snapshots.

</td>
<td headers="Avoid">
The snapshot retention policy is described later in the Atlas documentation.

</td>
</tr>
<tr>
<td headers="Use">
The following table lists which MongoDB versions and components the current releases of MongoDB Ops Manager support.

</td>
<td headers="Avoid">
The table below lists the MongoDB versions and components supported by the current releases of MongoDB Ops Manager.

</td>
</tr>
<tr>
<td headers="Use">
The most current versions of all drivers are located on the MongoDB Drivers site.

</td>
<td headers="Avoid">
The most current versions of all drivers are located on the MongoDB Developer Docs site: https://docs.mongodb.com/ecosystem/drivers/.

</td>
</tr>
<tr>
<td headers="Use">
You can obtain the API key by logging in to Atlas and clicking the Access Manager, then clicking the API Keys.

</td>
<td headers="Avoid">
You can obtain the API key from Atlas by selecting the API Keys tab on the Access Manager page. (Log in at https://cloud.mongodb.com/.)

</td>
</tr>
<tr>
<td headers="Use">
Contact MongoDB Support for any questions on Atlas' limits of MongoDB nodes per Network Peering connection.

</td>
<td headers="Avoid">
If you have questions on Atlas' limits of MongoDB nodes per Network Peering connection, click here

</td>
</tr>
<tr>
<td headers="Use">
The Connect dialog for a cluster provides the details to connect to a cluster using Compass.

</td>
<td headers="Avoid">
Download Compass from the Connect dialog.

</td>
</tr>
<tr>
<td headers="Use">
To learn more about link relations, see the Web Linking Specification.

</td>
<td headers="Avoid">
For more information on the Web Linking Specification, go to the IETF site.

</td>
</tr>
</table>