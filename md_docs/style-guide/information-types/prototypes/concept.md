---
title: Concept Page Prototype
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/information-types/prototypes/concept/
---

# Concept Page Prototype

This page provides general guidance and examples for Information Types. Verify the correct and consistent guidelines for each product with your team.

A concept page helps a user learn about a concept or new feature. The page intends to answer the following questions:

- "What is this?"

- "Why do I care?"

- "How does this work?"

The audience includes users who have never used a particular feature or command.

The title is typically a noun or noun phrase.

A concept page begins with a brief introduction that summarizes its contents, often called a short description. The short description explains a little about the concept and why the audience should care about it.

## Command Syntax

Optional.

If it's appropriate, you may include a code-block with a copyable prototype to familiarize users with command syntax.

```javascript
db.collection.<method>( {
   /* command fields */
} )
```

After the code block, provide a link to the corresponding reference or task page to provide readers with complete examples and behavior details. When possible, use includes to single-source code examples across related concept, task, and reference pages.

For concept pages that have multiple linked tasks, the code example should show the most common task we expect users to look for.

## Use Cases

This section includes a collection of use cases to explain "What do I do with this thing?" In general, use cases are short descriptions about how to use a feature. They set expectations for when and how you might use a feature and what differentiates this feature from other options.

## Behavior

This section includes information you need to know before using a feature. It can be as long or short as appropriate. Some examples of technical details include:

- Performance considerations and behavior alerts

- Support for a feature (for example, sharded cluster support or Versioned API compatibility)

- Version support

## Get Started

Link to the most common task pages related to this concept. Linking to all task pages isn't necessary here. The goal of this section is to make sure users can easily find common related tasks.

- Link one

- Link two

- Link three

## Details

This section is a brief unpacking of the technical details. It can be as long or short as appropriate. Generally, the information in this section is supplemental and should not be a major factor in a user's decision to use a feature.

## Learn More

This section appears on every information typed page. It does not replace inline linking, but is intended to augment the information on the page with related concepts, tasks, and reference material. Use it to link related pages that are not already linked above, such as reference information, technical deep dives, less commonly used task pages, or related concepts.