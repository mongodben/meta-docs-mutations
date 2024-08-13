---
title: Capitalization
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/capitalization/
---

# Capitalization

Be judicious and consistent in your use of capitalization. This topic provides general guidelines to help you decide when to capitalize a term.

To learn the correct capitalization of some common terms, see Alphabetical List of Terms.

For capitalization guidelines for items other than terms, see the table at the end of this topic.

## Capitalize Proper Nouns and Adjectives

Proper nouns and adjectives include the names of people, places, companies, organizations, products, languages, protocols, and some technologies, as well as trademarks.

Be aware that some of these names might have nonstandard or no capitalization. Always follow the capitalization that's used by the company, shown in a dictionary, or accepted as standard in the industry.

- Boolean

- Cloud Servers

- Ethernet

- Hong Kong

- Internet

- lighttpd

- Linux

- Microsoft Windows

- MongoDB

- OpenStack

- PuTTY

- RackConnect

- Service Advertising Protocol

- SQL Server

- Wi-Fi

- WordPress

For the correct capitalization of:

- MongoDB product names, see the MongoDB corporate website.

- Some commonly used third-party names, see Copyrights and Trademarks.

## Capitalize Most Abbreviations

Most abbreviated forms of terms use all capitals, although exceptions exist. Also, be aware that the corresponding spelled-out terms of abbreviations are often not capitalized. When in doubt about the capitalization of an abbreviation or its spelled-out term, consult a dictionary, industry style guide, reputable website, or editor. Following are some examples.

<table>
<tr>
<th id="Abbreviation">
Abbreviation

</th>
<th id="Spelled-out%20term">
Spelled-out term

</th>
</tr>
<tr>
<td headers="Abbreviation">
API

</td>
<td headers="Spelled-out%20term">
application programming interface

</td>
</tr>
<tr>
<td headers="Abbreviation">
fCV

</td>
<td headers="Spelled-out%20term">
feature compatibility version

</td>
</tr>
<tr>
<td headers="Abbreviation">
GB

</td>
<td headers="Spelled-out%20term">
gigabyte

</td>
</tr>
<tr>
<td headers="Abbreviation">
GHz

</td>
<td headers="Spelled-out%20term">
gigahertz

</td>
</tr>
<tr>
<td headers="Abbreviation">
ID

</td>
<td headers="Spelled-out%20term">
identificationNote: `_id` is never capitalized.

</td>
</tr>
<tr>
<td headers="Abbreviation">
I/O

</td>
<td headers="Spelled-out%20term">
input/output

</td>
</tr>
<tr>
<td headers="Abbreviation">
JSON

</td>
<td headers="Spelled-out%20term">
JavaScript Object Notation

</td>
</tr>
<tr>
<td headers="Abbreviation">
Kbps

</td>
<td headers="Spelled-out%20term">
kilobits per second

</td>
</tr>
<tr>
<td headers="Abbreviation">
REST

</td>
<td headers="Spelled-out%20term">
Representational State Transfer

</td>
</tr>
<tr>
<td headers="Abbreviation">
SaaS

</td>
<td headers="Spelled-out%20term">
software as a service

</td>
</tr>
<tr>
<td headers="Abbreviation">
SOA

</td>
<td headers="Spelled-out%20term">
service-oriented architecture

</td>
</tr>
<tr>
<td headers="Abbreviation">
WSDL

</td>
<td headers="Spelled-out%20term">
Web Services Description Language

</td>
</tr>
</table>To learn more, and for a list of common abbreviations, see Abbreviations.

## Capitalize Job Titles when Used as Titles

Within MongoDB technical documentation, use the following rules for capitalization in job titles:

<table>
<tr>
<th id="Use%20case">
Use case

</th>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Use%20case">
If you’re referring to a job role in general, don’t use initial capitals.

</td>
<td headers="Examples">
All support technicians will be allocated an account manager and a career coach.

</td>
</tr>
<tr>
<td headers="Use%20case">
Don’t use initial capitals where the title is being used as a description.

</td>
<td headers="Examples">
- The chief executive is Jane Brown and the associate director is Paul Woods.

- We have a new information developer.

- I’ll need to ask our sales director.

- I work as a software architect.

</td>
</tr>
<tr>
<td headers="Use%20case">
Use initial capitals where the term is serving as an actual title with the name of a person: just as you would on a business card or email signature.

</td>
<td headers="Examples">
- Chief Executive Jane Brown and Paul Woods, Associate Director, were both late.

- Attendee list:

  - Anna Collins, Editorial Director;

  - Shazeen Iqbal, Chief Financial Officer;

  - Pope Francis

</td>
</tr>
</table>

## Watch for Capitonyms

Some words have a different meaning depending on how they are capitalized. Make sure that you don't change the meaning of a word with an incorrect capitalization:

<table>

<tr>
<td>
File Transfer Protocol

</td>
<td>
Command-line FTP client

</td>
</tr>
<tr>
<td>
Kilobytes per second

</td>
<td>
Kilobits per second

</td>
</tr>
<tr>
<td>
Fifth month of the year

</td>
<td>
Modal verb

</td>
</tr>
<tr>
<td>
Representational State Transfer

</td>
<td>
State of motionlessness or inactivity

</td>
</tr>
</table>

## Capitalize Team Names

When you use team names in technical documents, use initial capitals as shown in the following table:

<table>
<tr>
<th id="Examples%20of%20initial%20capitals%20in%20team%20names">
Examples of initial capitals in team names

</th>
</tr>
<tr>
<td headers="Examples%20of%20initial%20capitals%20in%20team%20names">
The Support team handles making the change for you.

</td>
</tr>
<tr>
<td headers="Examples%20of%20initial%20capitals%20in%20team%20names">
Contact your Account Management team can tell you what the charge will be.

</td>
</tr>
<tr>
<td headers="Examples%20of%20initial%20capitals%20in%20team%20names">
The Documentation team is amazing!

</td>
</tr>
<tr>
<td headers="Examples%20of%20initial%20capitals%20in%20team%20names">
Contact Information Development <add email link> for instructions.

</td>
</tr>
</table>

## Capitalize UI Labels as shown on the UI

When you're documenting part of the interface within a procedure or other type of article or topic, match the capitalization used on the interface.

When you use terms from the interface as common nouns, don't capitalize the terms.

<table>
<tr>
<th id="Use">
Use

</th>
</tr>
<tr>
<td headers="Use">
Click the action cog to the left of the cluster name and select **Edit Cluster**.

</td>
</tr>
<tr>
<td headers="Use">
From the Atlas console, you can rename a cluster.

</td>
</tr>
</table>As an exception, any UI element that appears in all capitals should be initial capitalized in the documentation. It reads as shouting at the user otherwise.

## Capitalize the Names of Product Components as Appropriate

Follow the capitalization of major component names that Marketing, Legal, and the product teams have established.

Be wary of overcapitalization of product terms as not every feature or object in a product is a proper noun.

- Atlas enables users to create a *cluster*, not a *Cluster*.

- When the user creates a cluster, the user specifies a *cloud provider*, *tier*, and *region*, not a *Cloud Provider*, *Tier*, and *Region*.

- A user can create a *load balancer*, not a *Load Balancer*.

Many terms that might be capitalized in the UI aren't capitalized when used as common nouns. When in doubt, consult an existing style sheet, an editor, or the product team.

Follow these tips to help you determine whether a noun should be capitalized:

- Generally, if you can have more than one of something, it's a common noun and therefore not capitalized.

- When a common noun follows the name of a product or component, generally that noun isn't capitalized.

- When you refer generally to a component, you can use lowercase (as in the utility or the agent).

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
Zipit Backup Utility

</td>
</tr>
<tr>
<td headers="Examples">
Rate Limiting component

</td>
</tr>
<tr>
<td headers="Examples">
Identity service

</td>
</tr>
<tr>
<td headers="Examples">
servers

</td>
</tr>
<tr>
<td headers="Examples">
backups

</td>
</tr>
<tr>
<td headers="Examples">
containers

</td>
</tr>
<tr>
<td headers="Examples">
authentication

</td>
</tr>
</table>

## Don't Capitalize Common Nouns

Most of the time, you can determine whether a noun is proper or common. Sometimes you might capitalize product-specific terms even when they're really just being used as common nouns. A common noun denotes a whole class of something (*servers*) or a random member of a class (*a server*). As a general rule, if you can have more than one of something, it's a common noun and therefore not capitalized.

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
You can submit up to 10 messages in a single request, but you must encapsulate them in a JSON array.

</td>
<td headers="Don't%20use">
You can submit up to 10 Messages in a single Request, but you must encapsulate them in a JSON Array.

</td>
</tr>
<tr>
<td headers="Use">
Repose authentication provides caching for user tokens, roles, and groups.

</td>
<td headers="Don't%20use">
Repose Authentication provides caching for User Tokens, Roles, and Groups.

</td>
</tr>
</table>

## Don't Use All Capitals for Emphasis

To emphasize a term, show it in italics. To emphasize an important piece of information, consider setting it apart structurally, perhaps as a note.

CMOS 7.52: Capitals for emphasis

## Reference to Other Capitalization Guidelines

The following table provides links to other capitalization guidelines in the MongoDB Style Guide:

<table>
<tr>
<th id="Item">
Item

</th>
<th id="Reference">
Reference

</th>
</tr>
<tr>
<td headers="Item">
Code examples

</td>
<td headers="Reference">
Code Examples

</td>
</tr>
<tr>
<td headers="Item">
Diagram labels

</td>
<td headers="Reference">
Diagram Guidelines

</td>
</tr>
<tr>
<td headers="Item">
Glossary terms and definitions

</td>
<td headers="Reference">
Glossaries

</td>
</tr>
<tr>
<td headers="Item">
Key combinations

</td>
<td headers="Reference">
Keyboard Keys

</td>
</tr>
<tr>
<td headers="Item">
List items

</td>
<td headers="Reference">
List Items

</td>
</tr>
<tr>
<td headers="Item">
Placeholder (variable) text

</td>
<td headers="Reference">
Placeholder or Variable Text

</td>
</tr>
<tr>
<td headers="Item">
Table column headers and text

</td>
<td headers="Reference">
Tables

</td>
</tr>
<tr>
<td headers="Item">
Text following colons

</td>
<td headers="Reference">
Colons

</td>
</tr>
<tr>
<td headers="Item">
Text following em dashes

</td>
<td headers="Reference">
Dashes

</td>
</tr>
<tr>
<td headers="Item">
Titles and headings

</td>
<td headers="Reference">
Titles and Headings

</td>
</tr>
</table>