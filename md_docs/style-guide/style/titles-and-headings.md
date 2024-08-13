---
title: Titles and Headings
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/titles-and-headings/
---

# Titles and Headings

This topic provides guidelines for creating titles and headings in documentation.

## Capitalization

- Use *AP headline-style* capitalization for most titles and headings, including article, chapter, table, figure, and example titles, as well as section and procedure headings.

- Use *sentence-style* capitalization for titles of steps in step files.

## Guidelines for Headline-Style Capitalization

AP headline-style capitalization uses initial uppercase letters for the first, last, and all the significant words in the title.

Capitalize all words in the title except for the following types of words:

- Articles (*a*, *an*, *the*) unless the article is the first word in the title or follows a colon

- Coordinating conjunctions (*and*, *but*, *for*, *nor*, *or*, *yet*, *so*) unless the conjunction is the first word in the title

- Prepositions of any length, unless the preposition is the first or the last word in the title or is part of a verb phrase

- The word *to* in an infinitive phrase unless to is the first word in the title

- Second elements attached by hyphens to prefixes unless they're proper nouns or proper adjectives

- Words that always begin with a lowercase letter, such as literal command names or certain product or software names

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
Next Generation Cloud Servers Developer Guide

</td>
</tr>
<tr>
<td headers="Examples">
MongoDB Cloud DNS Getting Started Guide

</td>
</tr>
<tr>
<td headers="Examples">
Stand-alone Object Storage Guide

</td>
</tr>
<tr>
<td headers="Examples">
MongoDB Private Cloud powered by VMware Customer Handbook

</td>
</tr>
<tr>
<td headers="Examples">
Cloud Networks Release Notes

</td>
</tr>
</table>To learn more about the principles of headline-style capitalization, read section 8.159 of the *Chicago Manual of Style*.

### Style and Structure

Use the guidelines in this section to create effective and consistent titles and headings. The following guidelines apply to all titles and headings; special considerations for stand-alone articles, product guides, and tables, figures, and examples follow this list.

- Create succinct, meaningful, descriptive titles and headings, and place the most important words first.

- Ensure that each title and heading is unique. Identical titles, even between documentation sets, might compete in search results.

- Don't include "MongoDB" in a title unless the page is a product landing page.

- Include articles, prepositions, and punctuation as needed for clarity. However, avoid using an article (*a*, *an*, or *the*) as the first word.

- Avoid showing both an abbreviation and its spelled-out term in a title or heading. To help control the length of titles and headings, show the abbreviation in the title or heading and then define it in the first paragraph of the text.

- If you show a literal term (such as a command or option name) in a title or heading, follow it with an appropriate noun.

- Don't end a title or heading with a colon or period. If the title or heading is in the form of a question, end it with a question mark.

- Don't apply font treatments (bold, italics, or monospace) to text in a title or heading.

- Don't include trademark symbols in titles or headings. Show the symbol on the first use of the trademark in text.

- Avoid having only a single heading at any level (for example, a single subsection in an article or section). If you find that you have a single heading at any one level, consider whether you can reorganize the information to either eliminate the heading or add a second one at that level.

- Avoid having more than two levels of sections within an article or topic. If you use more than two levels of sections, consider whether you can reorganize to make the structure flatter.

- Don’t "stack" titles or headings. That is, don’t immediately follow a title or heading with another title or heading. Text should always intervene between them. Ensure that such text is meaningful. If it is just filler text, consider whether you can restructure the content.

- Use a consistent grammatical structure for the titles and headings of specific types of content:

  <table>
  <tr>
  <th id="Type">
  Type

  </th>
  <th id="Grammatical%20structure">
  Grammatical structure

  </th>
  <th id="Stand-alone%20article%20examples">
  Stand-alone article examples

  </th>
  <th id="Product%20guide%20examples">
  Product guide examples

  </th>
  </tr>
  <tr>
  <td headers="Type">
  Conceptual

  </td>
  <td headers="Grammatical%20structure">
  Any grammatical structure that's appropriate, except a verb, gerund, or infinitive

  </td>
  <td headers="Stand-alone%20article%20examples">
  Linux distributions

  Best practices for backing up your data

  </td>
  <td headers="Product%20guide%20examples">
  Core concepts

  How monitoring works

  Limitations of detaching from MongoDB networks

  </td>
  </tr>
  <tr>
  <td headers="Type">
  Step-by-step instructions (a task)

  </td>
  <td headers="Grammatical%20structure">
  An imperative verb

  For specific guidelines for headings within tasks, see Tasks.

  </td>
  <td headers="Stand-alone%20article%20examples">
  Identify network interfaces on Linux

  Prepare data disks on servers running Windows

  Set up Mobile Sync for Webmail

  </td>
  <td headers="Product%20guide%20examples">
  Sign up for a MongoDB Atlas account

  </td>
  </tr>
  <tr>
  <td headers="Type">
  Tutorial or high-level process

  </td>
  <td headers="Grammatical%20structure">
  A gerund

  </td>
  <td headers="Stand-alone%20article%20examples">
  Understanding logrotate

  Customizing Apache web logs

  </td>
  <td headers="Product%20guide%20examples">
  Working with your first message queue

  </td>
  </tr>
  <tr>
  <td headers="Type">
  Reference

  </td>
  <td headers="Grammatical%20structure">
  A plural noun or a noun phrase

  </td>
  <td headers="Stand-alone%20article%20examples">
  Permissions matrix for Cloud Networks

  MongoDB Auto Scale glossary

  </td>
  <td headers="Product%20guide%20examples">
  Environment variables for the nova and supernova clients

  Restore operations

  cURL command summary

  </td>
  </tr>
  <tr>
  <td headers="Type">
  Troubleshooting

  </td>
  <td headers="Grammatical%20structure">
  A grammatical structure that's appropriate for the type of content (a troubleshooting topic can contain task, tutorial, concept, or reference information)

  </td>
  <td headers="Stand-alone%20article%20examples">
  Troubleshoot alarms

  Service troubleshooting on Linux

  </td>
  <td headers="Product%20guide%20examples">
  Troubleshooting

  </td>
  </tr>
  <tr>
  <td headers="Type">
  FAQ

  </td>
  <td headers="Grammatical%20structure">
  A descriptive noun or noun phrase, followed by *FAQ*

  </td>
  <td headers="Stand-alone%20article%20examples">
  MongoDB Cloud Billing FAQ

  Scheduled images FAQ

  </td>
  <td headers="Product%20guide%20examples">
  Not applicable

  </td>
  </tr>
  </table>

### Standalone Articles

In addition to the preceding guidelines, use the following guidelines when creating titles and headings for stand-alone articles on the Support site or in other collections of documentation:

- Create article titles that don’t rely on body text or other titles for their meaning (that are, in other words, independent of context). Users should be able to tell from a title whether the information in the article is relevant to their needs. Avoid ambiguous one-word titles, such as "Overview."

- Don't number titles to indicate their placement in a series of articles. Indicate the order of articles within the content of the article, referring users to information that they should have read previously before reading the current article. Use links to provide navigation to preceding and following articles in the series.

- Start with the highest level of heading that is approved for headings (for example, h3), and do not skip heading levels.

### Product Guides

In addition to the preceding guidelines, use the following guidelines when creating titles and headings for sections in product guides:

- If possible, limit titles and headings to 60 characters for legibility in the TOC pane.

- Consider that titles and headings are written within the context of the content set in which they are presented. Therefore, you can usually omit "context-setting" terms. For example, if the content set is about servers, you can usually omit "for servers" from the title or heading. (For example, "Attach a network to a server" can be shortened to "Attach a network" with no loss of clarity.)

- Define consistent heading levels, and do not skip levels.

## Tables, Figures, and Examples

As a general rule, tables, figures, and examples should have titles (also called captions). However, tables, figures, and examples in procedures and tutorials don't normally require titles.

In addition to the preceding guidelines, use the following guidelines when creating titles for tables, figures, and examples:

- Place the title above the table, figure, or example, not below it.

- Tag the title as bold.

- Avoid using a title that duplicates an article or section title.

### Text Following Titles and Headings

Don’t immediately follow a title or heading with another title or heading. Instead, follow a title or heading with body text.

The body text must be independent from the title or heading. Don't use a title or heading as an antecedent in the sentence that follows it. That is, be sure to repeat the subject in the first sentence that follows the title or heading, rather than using a pronoun that refers to the title or heading as its antecedent.

<table>
<tr>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Use">
**Identify network interfaces on Linux**

This article briefly describes how to identify which network interfaces on a Linux server are associated with which IP addresses.

</td>
<td headers="Don't%20use">
**Identify network interfaces on Linux**

This article briefly describes how to do this.

</td>
</tr>
</table>

### Tables of Contents

In addition to using the preceding guidelines when creating titles and headings, use the following guidelines when creating a table of contents (TOC) for a collection of content:

- Entries in the TOC should link only to sections in the content. Don't include a link to an outside resource in the TOC.

- The text of a TOC entry should align with the text of the title or heading to which it links. If the link needs to be shorter, consider shortening the title or heading or providing a more concise title or heading for the TOC. An alternate TOC title or heading should convey the same intent of the full title or heading. To learn more, see Table of Contents Labels.

  ```rst
  .. toctree::
     :titlesonly:

     Install the Operator </installation>
     Deploy Ops Manager Resources </om-resources>
     Deploy MongoDB Database Resources </mdb-resources>
     /tutorial/modify-resource-image
     /reference
     Release Notes </release-notes>
     MongoDB Community Kubernetes Operator <https://github.com/mongodb/mongodb-kubernetes-operator>
  ```

- Don't manually format the TOC. TOC formatting must be consistent and controlled by the code.