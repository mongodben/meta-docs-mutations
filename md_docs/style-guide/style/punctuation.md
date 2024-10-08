---
title: Punctuation
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/punctuation/
---

# Punctuation

Use punctuation correctly and consistently. This section provides guidelines for using punctuation in MongoDB documentation. For basic rules about punctuation, see section 5, Grammar and Usage in the *Chicago Manual of Style*.

## Ampersands

Don't use an ampersand (&) in text or headings to mean *and* unless you're referring to the symbol on the UI. In the following example, the button name on the UI includes an ampersand (&):

To continue, click **Save & Go to Step 3**.

## Colons

Use the following guidelines for colons:

- Use a colon at the end of a sentence that introduces a list, table, figure, or example. If another sentence intervenes between the introduction and the thing being introduced, use a period instead of a colon.

- Use a colon at the end of the step to introduce substeps, a bullet list, or code that the user is expected to enter.

- In a list item, if you need to separate an initial term or phrase from the information that follows it, use a colon. For example:

  **Public**: This setting allows any two servers with public IP addresses to be load balanced. These can be nodes outside of the MongoDB network, but if they are, standard bandwidth rates apply.

- Don't use a colon at the end a table column header, a title, or a heading.

- Avoid using colons in sentences. You can almost always use two sentences instead. If you do use a colon in a sentence, however, don't capitalize the word that follows the colon unless the word is proper or is the beginning of a quotation.

- If a title or heading includes a colon, capitalize the first word that follows the colon, regardless of its part of speech.

- When you use a colon in a sentence, use lowercase for the first word that follows the colon unless it is a proper noun. When the colon introduces two or more sentences, a quotation, or question, capitalize the first word after the colon (from the Chicago Manual of Style 6.63, v17).

## Commas

Use the following guidelines for commas. For basic comma usage, see section 6.16, Commas in the *Chicago Manual of Style*.

<table>
<tr>
<th id="Guideline">
Guideline

</th>
<th id="Correct">
Correct

</th>
<th id="Incorrect">
Incorrect

</th>
</tr>
<tr>
<td headers="Guideline">
In a series of three or more items, use a serial comma (that is, precede the conjunction with a comma).

</td>
<td headers="Correct">
You can upgrade, migrate, and integrate the product.

</td>
<td headers="Incorrect">
You can upgrade, migrate and integrate the product.

</td>
</tr>
<tr>
<td headers="Guideline">
Don't use only a comma to separate independent clauses. Doing so creates a *comma splice*.

If you join independent clauses, insert a coordinating conjunction (such as *and*) between them and precede the conjunction with a comma.

</td>
<td headers="Correct">
Click **Options**, and then click **Allow Fast Saves**.

CentOS 6 comes with Apache 2.2.3 and PHP 5.1.6, and you can install them by using the default CentOS Package Manager, `yum`.

</td>
<td headers="Incorrect">
Click **Options**, then click **Allow Fast Saves**.

CentOS 6 comes with Apache 2.2.3 and PHP 5.1.6, you can install them by using the default CentOS Package Manager, `yum`.

</td>
</tr>
<tr>
<td headers="Guideline">
Use a comma to set off a nonrestrictive clause (one that begins with *which*).

Don't use a comma to set off a restrictive clause (one that begins with *that*).

</td>
<td headers="Correct">
The hourly backups are rolled into a nightly backup, which is retained for two days. *(nonrestrictive)*

Enter the username and password that you just created. *(restrictive)*

</td>
<td headers="Incorrect">
The hourly backups are rolled into a nightly backup which is retained for two days.

Enter the username and password, that you just created.

</td>
</tr>
<tr>
<td headers="Guideline">
Use a comma to separate an introductory word, phrase, or clause from the rest of the sentence.

</td>
<td headers="Correct">
When you check your email with an IMAP connection, you're accessing and managing your email directly from the email server.

However, you can easily update the version by using the WordPress management dashboard.

Unlike the other alarms in this list, you set the network check alarm variable upon network check creation.

To learn more, see Upgrading Ops Manager.

</td>
<td headers="Incorrect">
When you check your email with an IMAP connection you're accessing and managing your email directly from the email server.

However you can easily update the version by using the WordPress management dashboard.

Unlike the other alarms in this list you set the network check alarm variable upon network check creation.

To learn more see Upgrading Ops Manager.

</td>
</tr>
<tr>
<td headers="Guideline">
Don't use a comma between the verbs in a compound predicate.

</td>
<td headers="Correct">
These open-source Python clients run on Linux or Mac OS X systems and are easy to learn and use.

</td>
<td headers="Incorrect">
These open-source Python clients run on Linux or Mac OS X systems, and are easy to learn and use.

</td>
</tr>
<tr>
<td headers="Guideline">
When a comma is required after a quotation that's embedded in text, place the comma inside the closing quotation mark.

</td>
<td headers="Correct">
In the section called "Parameters," enter the values for length, width, and height.

</td>
<td headers="Incorrect">
In the section called "Parameters", enter the values for length, width, and height.

</td>
</tr>
<tr>
<td headers="Guideline">
Use commas in numbers with five or more digits. However, don't use commas in the following types of numbers: addresses, fractional parts of decimal numbers, page numbers, literal representations of user-entered values or displayed values

Don't use European-style numbering, which uses commas in the place of periods. For example, use 3.14159, not 3,14159.

</td>
<td headers="Correct">
9001 N IH 35

1452.7532

page 1055

1024 bytes

</td>
<td headers="Incorrect">
9,001 N IH 35

1,452.753,2

page 1,055

1,024 bytes

</td>
</tr>
<tr>
<td headers="Guideline">
When city and state names are embedded in a sentence, use a comma after the city and the state.

</td>
<td headers="Correct">
The company headquarters were in Kansas City, Missouri, before the merger.

</td>
<td headers="Incorrect">
The company headquarters were in Kansas City, Missouri before the merger.

</td>
</tr>
<tr>
<td headers="Guideline">
When a month, day, and year are embedded in a sentence, use a comma before and after the year. When only the month and year compose the date, omit the commas unless the syntax would ordinarily require a comma following the year.

</td>
<td headers="Correct">
The company acquired a German subsidiary on July 15, 2009, and is negotiating the purchase of a small Japanese company.

The publications plan was printed in November 2010 in Austin.

In December 2012, the database restoration failed.

</td>
<td headers="Incorrect">
The company acquired a German subsidiary on July 15, 2009 and is negotiating the purchase of a small Japanese company.

The publications plan was printed in November, 2010, in Austin.

In December 2012 the database restoration failed.

</td>
</tr>
</table>

## Dashes

An *em dash* is the longest dash. You can use em dashes to set off a long qualifier in the middle of a sentence if the use of commas would hinder readability. If you use em dashes for this purpose, don't use spaces around them. (For an example, see the second paragraph in the following section, "Ellipses.")

Don't capitalize the word following an em dash, unless the word is proper.

Don't use an em dash to separate a long sentence into two parts. Instead, create two sentences.

An *en dash* is longer than a hyphen and shorter than an em dash. Most often, you might use an en dash to show a range of numbers in a table or figure. For example, 10–20 diagrams.

To show a range of numbers in text, use *to* or *through* instead of an en dash.

## Ellipses

Use an ellipsis (...) in syntax or to indicate omitted code in code examples.

Don't use an ellipsis in header text of table columns or when showing the name of an interface element—such as a text box, menu, menu command, or command button—even if the ellipsis is displayed on the interface. For example, don't use an ellipsis as follows:

- On the **File** menu, click **Open...**.

- Do this ... *(column header)*

## Exclamation points

Avoid using exclamation points.

## Hyphens

This section provides general guidelines for hyphenation. For guidelines about using dashes, see Dashes.

- Hyphens in compound modifiers

- Hyphens with prefixes

### Hyphens in compound modifiers

When two or more words precede and modify a noun as a unit (also called a *compound modifier*), use hyphens according to the following guidelines.

- To clarify meaning, use a hyphen. For example, *high-level-language compiler* is clearer than *high level language compiler.*

- Words that you hyphenate as compound modifiers preceding a noun might not be hyphenated in other parts of a sentence or when used as another part of speech. Hyphenate only if needed for clarity. For example, *local-level attributes* but *attributes defined at the local level*.

  **Note:** One exception is *up-to-date*, which is hyphenated in any position in a sentence.

- If the first component of a compound modifier is a number, use a hyphen. For example, *32-bit operating system*.

- If the first word of a compound modifier is an adverb ending in *-ly*, don't hyphenate the modifier. For example, *fully qualified domain name*.

- If one of the elements of a compound modifier is a trademark, don't hyphenate the modifier. For example, *Java specific*, not *Java-specific*.

### Hyphens with prefixes

Words with prefixes aren't usually hyphenated. However, a hyphen might be necessary in the following cases:

- You need to distinguish between homographs, such as *re-create* and *recreate*.

- The last letter of the prefix and the first letter of the root word are the same. Exceptions are words such as *reenter* and *preemptive*, which aren't likely to be misread.

- The product team has hyphenated a term with a prefix, and you need to follow suit in the docs for consistency with the interface. Whenever possible, work with the teams to use preferred spelling.

For the correct formatting of a specific word, see a dictionary or Alphabetical List of Terms. For more information about hyphenating prefixes, see The Chicago Manual of Style.

## Parentheses

Avoid parentheses in running text. Parenthetical text can distract the reader from the main idea of the sentence and disrupt the flow of the sentence. When possible, put parenthetical information in a separate sentence.

Following are some acceptable uses for parentheses:

- To define an abbreviation

- To show a special character

- To show examples

- To show a concise phrase that qualifies a term, title, or step

Don't add *(s)* or *(es)* to the end of a noun to indicate the possibility of more than one item. Use the singular form or the plural form, or use both forms joined by a conjunction.

<table>
<tr>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Examples">
An access control list (ACL) allows access from an outside network into the ObjectRocket system.

Object names can't contain characters such as dollar signs ($) and question marks (?).

DNS is analogous to a phone book in that it assigns a numerical identifier (for example, 210.48.108.35) to a particular name (for example, www.diversity.net.nz).

1. *(Optional)* Enter first and last name information for the mailbox owner.

You can submit up to 10 messages (the default) in a single request.

</td>
</tr>
</table>

## Periods

Use the following guidelines for periods. For basic period usage, see a grammar reference, section 6.12, Periods in the *Chicago Manual of Style*.

- Use a period at the end of a declarative or imperative sentence, and insert only one space after the period.

- Place periods inside quotation marks, unless the quotation marks are part of a literal string. In such cases, place the period outside the quotation mark.

- Use periods in list items as follows:

  - If all of the items in a list are sentences, including imperative statements, end each item with a period.

  - If all of the items in a list are fragments, don't end the items with a period.

  - In a list of fragments, some or all of which are followed by sentences, end every fragment and sentence in the list with a period. For example, see the "Lists" topic.

- Use periods with abbreviations that could be misread as a word, such as *in.* (for *inch*).

- Precede a file name extension with a period.  Also, assume that the period in a file name extension is pronounced as *dot*, and use the indefinite article *a*. For example, a .**ini** file.

- Don't end a title or a heading with a period.

## Quotation marks

Refer to quotation marks as *quotation marks*, not as *quote marks* or *quotes*.

Use single and double quotation marks according to the following guidelines:

- Use quotation marks in user entries or syntax only if the software requires the quotation marks.

- Use quotation marks in message text only if the product shows quotation marks in the generated message. Use code font (monospace) to format messages.

- If you use a term in a unique or qualified sense, use double quotation marks in text only at its first occurrence, and omit the quotation marks in subsequent occurrences of the term. For example:

  The spelling checker "learns" the word. After it learns the word, the spelling checker ignores subsequent occurrences of the word in the document.

- Include appropriate punctuation, such as periods and commas, inside quotation marks unless the quotation marks are part of the syntax that the user must type.

- Don't use quotation marks for emphasis. Use italics instead, or other formatting as described in the "Text formatting" topic.

- Use quotation marks to enclose text that's used verbatim from another source, or to enclose quotations from people.

## Semicolons

Avoid using semicolons, which are often misused and, even when used correctly, can make sentences longer and more difficult to understand.

- Instead of connecting independent clauses with a semicolon, break them into separate sentences.

- Instead of connecting more than two items with semicolons, create a list.

## Slashes

Don't use a slash mark (/) to present a choice among, or a series of, actions or objects. Rewrite the phrase to eliminate the slash mark. Exceptions are established terms like *client/server* and *read/write*.

Don't use a slash in dates. For information about how to format dates, see Dates.

<table>
<tr>
<th id="Correct">
Correct

</th>
<th id="Incorrect">
Incorrect

</th>
</tr>
<tr>
<td headers="Correct">
You can choose Cloud Backups, Cloud Files, or both.

</td>
<td headers="Incorrect">
You can choose Cloud Backups and/or Cloud Files. You can choose Cloud Backups/Files.

</td>
</tr>
<tr>
<td headers="Correct">
To access your computer, plug it in, log in to the operating system, and type your password.

</td>
<td headers="Incorrect">
To access your computer, plug in the computer/log on/type your password.

</td>
</tr>
</table>