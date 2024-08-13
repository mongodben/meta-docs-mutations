---
title: Reference Page Prototype
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/information-types/prototypes/reference/
---

# Reference Page Prototype

This page provides general guidance and examples for Information Types. Verify the correct and consistent guidelines for each product with your team.

A reference page provides quick information to experienced users of a product. Reference pages may describe the use of a method, operator, or database command. Release notes are another example of reference page.

Usually, the title of a reference page is the name of the command, operator, or method it describes.

## Definition

A reference page begins with a brief introduction summarizing its contents, often called a short description. The short description explains a little about how the reference material is used, and may link to a concept or task page.

## Compatibility

Optional.

A list of MongoDB editions that support the referenced method, operator, or database command:

- MongoDB Atlas: The fully managed service for MongoDB deployments in the cloud

If Atlas supports the command or functionality, specify a level of compatibility such as one of the following:

- Available in all clusters

- Available only in certain clusters

- Available in no clusters

To see an example, see aggregate Compatibility.

- MongoDB Enterprise: The subscription-based, self-managed version of MongoDB

- MongoDB Community: The source-available, free-to-use, and self-managed version of MongoDB

On the MongoDB Server documentation, you can use the following includes for the list of supported MongoDB editions:

- `.. include:: /includes/fact-environments-atlas-only.rst`

- `.. include:: /includes/fact-environments-onprem-only.rst`

On the MongoDB Drivers documentation, you can use `.. sharedinclude:: dbx/platform-support/atlas-connect-compatible-deployment.rst`.

## Syntax

This section includes the sample syntax with the required parameters.

```javascript
db.adminCommand(
   {
     addShard: "<replica_set>/<hostname><:port>",
     maxSize: <size>,
     name: "<shard_name>"
   }
)
```

## Command Fields

The command takes the following fields:

<table>
<tr>
<th id="Field">
Field

</th>
<th id="Type">
Type

</th>
<th id="Necessity">
Necessity

</th>
<th id="Description">
Description

</th>
</tr>
<tr>
<td headers="Field">
Parameter

</td>
<td headers="Type">
String

</td>
<td headers="Necessity">
Required

</td>
<td headers="Description">
String

</td>
</tr>
</table>

## Behaviors

Optional.

Behaviors should apply only to the operator described on this page.

## Examples

Optional.

This section could contain examples of the most common use cases. Use includes for Reference and Task page examples, so we write the examples once, present them consistently throughout the documentation, and can update them easily.

If an example is shared between task and reference, you should write it as an include.

## Learn More

This section appears on every information typed page. It does not replace inline linking, but is intended to augment the information on the page with related concepts, tasks, and reference material. Use it to link related pages that are not already linked above, such as reference information, technical deep dives, less commonly used task pages, or related concepts.