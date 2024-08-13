---
title: Abbreviations
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/abbreviations/
---

# Abbreviations

- Unless an abbreviation is common, spell out the words of the abbreviation on the first use in an article or topic.

  In FAQ documents, treat every occurrence of a term as the first use (that is, spell out the term and show the abbreviation in parentheses on every occurrence).

- Show the abbreviation in parentheses after the spelled-out term on the first appearance on the page.

  access control list (ACL)

- Use the abbreviation on subsequent uses on the page.

- If you introduce an abbreviation, use it; don't alternate between the abbreviation and the spelled-out term.

- Use the `:abbr:` role to embed the words as a hover option for the first mention of an abbreviation in a paragraph.

  ```rst
  :abbr:`ACL (access control list)`
  ```

  You may use `:abbr:` role on every subsequent reference, if desired. You can't use this role within any other text formatting notation in reStructuredText. The abbreviation could also be defined within the toolchain as a source_constant or a substitution.

  Toolchain substitutions would be in the `conf.py` for Sphinx / Giza-based repos and `snooty.toml` for Snooty-based repos.

- Don't capitalize the spelled-out term unless it's a proper name or normally capitalized.

  You spell out *AJAX* as *Asynchronous JavaScript and XML*, but spell out *ACL* as *access control list*.

- Use the following guidelines related to abbreviations.

<table>
<tr>
<th id="Guideline">
Guideline

</th>
<th id="Use">
Use

</th>
<th id="Don't%20use">
Don't use

</th>
</tr>
<tr>
<td headers="Guideline">
Don't show both the spelled-out term and its abbreviation in a title or heading. In most cases, use the abbreviation in the title or heading and show the spelled-out term and its abbreviation on first use in the text.

</td>
<td headers="Use">
**Adding an ACL**

An access control list (ACL) allows access from an outside network into the ObjectRocket system.

</td>
<td headers="Don't%20use">
**Adding an access control list (ACL)**

An ACL allows access from an outside network into the ObjectRocket system.

</td>
</tr>
<tr>
<td headers="Guideline">
Use only established abbreviations. Don't create new ones.

</td>
<td headers="Use">
hybrid cloud

</td>
<td headers="Don't%20use">
HC

</td>
</tr>
<tr>
<td headers="Guideline">
Don't use abbreviated forms of MongoDB product names.

However, if you think that a user might use an abbreviated name in a search, you can tag the document with the abbreviation.

</td>
<td headers="Use">
Cloud Provider Snapshots

</td>
<td headers="Don't%20use">
CPS

</td>
</tr>
<tr>
<td headers="Guideline">
If an abbreviation is used as part of a compound modifier, hyphenate it as you would a word.

For more information, see Hyphens in compound modifiers.

</td>
<td headers="Use">
100-Mbps rate

</td>
<td headers="Don't%20use">
100 Mbps rate

</td>
</tr>
<tr>
<td headers="Guideline">
Don't surround abbreviations with quotation marks.

</td>
<td headers="Use">
OS

</td>
<td headers="Don't%20use">
"OS"

</td>
</tr>
<tr>
<td headers="Guideline">
Use periods only if the abbreviation normally has them (for example, *etc.*, although this should not be used in MongoDB content) or could otherwise be misread as a word, such as *in.* (for *inch*).

</td>
<td headers="Use">
FAQ

</td>
<td headers="Don't%20use">
F.A.Q.

</td>
</tr>
<tr>
<td headers="Guideline">
Don't use an abbreviation as a verb.

</td>
<td headers="Use">
Use FTP to copy the file to the server.

</td>
<td headers="Don't%20use">
FTP the file to the server.

</td>
</tr>
<tr>
<td headers="Guideline">
Avoid using abbreviations in the possessive. Instead, treat the abbreviation as an adjective or put it in a prepositional phrase.

</td>
<td headers="Use">
Type the DBA password.

Type the password of the DBA.

</td>
<td headers="Don't%20use">
Type the DBA's password.

</td>
</tr>
<tr>
<td headers="Guideline">
To form the plural of an abbreviation, except for a unit of measure, append a lowercase *s* without an apostrophe.

For most abbreviations of units of measure, the singular and plural forms are the same (for example, 1 pt and 10 pt).

If an acronym already represents a plural noun, don't add an *s*.

</td>
<td headers="Use">
user IDs

10 mm

FAQ

</td>
<td headers="Don't%20use">
user ID's

10 mms

FAQs

</td>
</tr>
<tr>
<td headers="Guideline">
For abbreviated units of measure, insert a space between the number and the abbreviation. Insert a hyphen if the phrase is a compound modifier.

</td>
<td headers="Use">
256 MB

100-GB drive

</td>
<td headers="Don't%20use">
256MB

100GB drive

100 GB drive

</td>
</tr>
<tr>
<td headers="Guideline">
Don't use Latin abbreviations or non-English words and phrases. For more information, see Avoid Obscure Non-English Words and Abbreviations.

</td>
<td headers="Use">
for example

</td>
<td headers="Don't%20use">
e.g.

</td>
</tr>
</table>
## Abbreviations of Byte and Bit

*Byte* is abbreviated with an uppercase *B*. *Bit* is abbreviated with a lowercase *b*. For example, *gigabyte* is abbreviated as *GB*, and *gigabit* is abbreviated as *Gb*.

- Abbreviate capacity when a number preceeds the unit.

- Spell out the term when used on its own.

If you want to emphasize *bit* or *byte*, use the spelled-out term rather than or in addition to the abbreviation.

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
When the host reads a page into memory larger than 100 MB, it displays this value rounded up to the nearest megabyte (MB) in the summary report.

</td>
</tr>
<tr>
<td headers="Examples">
The unit of value for this alarm is megabits per second (Mbps).

</td>
</tr>
</table>

## Common Abbreviations

A common abbreviation is either an industry-standard abbreviation or one that is well known to your target audience. Following are some common abbreviations in the computer industry. You don't need to spell out these terms on first use, unless you think the abbreviation is unfamiliar to your audience. If you use `:abbr:` roles, you can use them on common terms as a subtle aid in user understanding.

- API

- ASCII

- BIOS

- BSON

- CD

- CD-ROM

- CGI

- CLI

- CPU

- CSS

- CSV

- DNS

- DVD

- FAQ

- FTP

- GB

- GHz

- GMT

- GNU

- GUI

- GUID

- HTML

- HTTP

- HTTPS

- ID

- IEEE

- IMAP

- I/O

- IP

- JSON

- KB

- Kbps

- KBps

- kHz

- KMS

- LAN

- LDAP

- MB

- MHz

- NIC

- NTFS

- OLE

- OS

- PEM

- PDF

- PHP

- POP

- PROD

- PSA

- RAM

- REST

- ROM

- SaaS

- SGML

- SMTP

- SQL

- SSD

- SSH

- SSL

- TCP

- TCP/IP

- TLS

- TTL

- URI

- URL

- USB

- USD

- UTC

- VLAN

- WAN

- XFS

- XML

- YAML

- ZIP