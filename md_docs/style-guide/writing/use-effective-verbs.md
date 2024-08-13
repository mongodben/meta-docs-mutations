---
title: Use Effective Verbs
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/writing/use-effective-verbs/
---

# Use Effective Verbs

Verbs carry the action in a sentence. They make your content come alive for users. To make the biggest impact with your writing, use strong, simple, action verbs. See the following sections for specific guidelines.

## Use Action-Oriented Verbs

Verbs are supposed to carry the action in a sentence. When you use verbs like *be*, *have*, *make*, or *do* (and their variants), or when you use gerunds (*-ing* words), nouns carry the action and weaken the meaning. Replace weak verbs and gerunds with strong, action-oriented verbs to restore focus  to verbs from nouns. Relying on verbs rather than nouns usually makes sentences shorter, clearer, and more direct.

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
MongoDB **leads** the industry.

</td>
<td headers="Avoid">
MongoDB **is** the industry leader.

</td>
</tr>
<tr>
<td headers="Use">
Role-Based Access Control (RBAC) **restricts** service access to authorized users.

</td>
<td headers="Avoid">
Role-Based Access Control (RBAC) **is** a method of restricting service access to authorized users.

</td>
</tr>
<tr>
<td headers="Use">
If the node **can't access the Internet**, the installation process fails.

</td>
<td headers="Avoid">
If the node **doesn't have Internet access**, the installation process fails.

</td>
</tr>
<tr>
<td headers="Use">
To create a server, **specify** a name, flavor, and image.

</td>
<td headers="Avoid">
You create a server **by specifying** a name, flavor, and image.

</td>
</tr>
<tr>
<td headers="Use">
When you **create** a server, ...

</td>
<td headers="Avoid">
When **creating** a server, ...

</td>
</tr>
</table>

## Avoid Nouns Built from Verbs

Many nouns are built from verbs, for example, *description* and *explanation*. Such nouns are called *nominalizations*. Some sentences include a nominalization *and* a verb. Change the nominalization back into a verb and omit the existing verb to simplify those sentences.

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
The following table **describes** each of the products.

</td>
<td headers="Avoid">
The following table **provides a description of** each of these products.

</td>
</tr>
<tr>
<td headers="Use">
**Install** the product by completing the following tasks.

</td>
<td headers="Avoid">
**Perform the installation** of the product by completing the following tasks.

</td>
</tr>
<tr>
<td headers="Use">
The program **encrypts** user IDs and passwords.

</td>
<td headers="Avoid">
The program **enables the encryption of** user IDs and passwords.

</td>
</tr>
</table>

## Use the Simplest Tense

Simple verbs, such as verbs in the present tense, are easier to read and understand than complex verbs, such as verbs in the progressive or perfect tense, or verbs combined with helping verbs (such as *can*, *may*, *might*, *must*, and *should*).

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
Before you perform this task, **complete** the prerequisites.

</td>
<td headers="Avoid">
Before you perform this task, you **should have completed** the prerequisites.

</td>
</tr>
<tr>
<td headers="Use">
To start, three ports **are** open: `ssh`, `http`, and `https`.

</td>
<td headers="Avoid">
To start, you **are going to have** three ports open: `ssh`, `http`, and `https`.

</td>
</tr>
<tr>
<td headers="Use">
If you **use** a Red Hat distribution, iptables works a little differently.

</td>
<td headers="Avoid">
If you **are using** a Red Hat distribution, iptables works a little differently.

</td>
</tr>
</table>

## Use Modal Verbs Accurately

Modal verbs are helping verbs that further modify the action or meaning of the main verb. If you need to use the following helping or modal verbs, use them accurately and consistently:

<table>
<tr>
<th id="Modal%20verb">
Modal verb

</th>
<th id="Description">
Description

</th>
<th id="Example">
Example

</th>
</tr>
<tr>
<td headers="Modal%20verb">
can

</td>
<td headers="Description">
Indicates the ability to perform an action.

</td>
<td headers="Example">
You **can** customize Atlas clusters to achieve a wide range of performance, durability, availability, and efficiency goals.

</td>
</tr>
<tr>
<td headers="Modal%20verb">
may

</td>
<td headers="Description">
Indicates permission.

</td>
<td headers="Example">
If you need space, you **may** uninstall the program.

</td>
</tr>
<tr>
<td headers="Modal%20verb">
might

</td>
<td headers="Description">
Indicates probability or possibility.

</td>
<td headers="Example">
A service **might** expose endpoints in different regions.

</td>
</tr>
<tr>
<td headers="Modal%20verb">
must

</td>
<td headers="Description">
Indicates the necessity of an action.

In general, use the imperative mood. It implies the subject *you* and doesn't require *must* but still indicates necessity.

</td>
<td headers="Example">
The worker **must** delete the message when work is done.

</td>
</tr>
<tr>
<td headers="Modal%20verb">
should

</td>
<td headers="Description">
Indicates a recommendation or an expectation.

Avoid using should, because it implies uncertainty or could imply a best practice (which we might or might not want to do).

</td>
<td headers="Example">
To avoid losing a claim in the middle of processing a message, clients **should** periodically renew claims during long-running batches of work.

</td>
</tr>
</table>

## Use Single-Word Verbs

When possible, use single-word verbs rather than phrasal verbs (verbs followed by prepositions or adverbs).

Use *omit* rather than *leave out*, or shorten *start up* to *start*. One-word verbs are easier to understand and to translate.

If you must use a phrasal verb, keep the parts of the verb together unless that changes the meaning of the sentence. Some acceptable phrasal verbs are *back up*, *log in*, *set up*, *shut down*, and *work around*.

Don't turn a phrasal verb into a single-word verb.

Don't use *login*, *setup*, or *workaround* as verbs. These single-word terms should be used only as nouns or adjectives.

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
**Determine** the type of encryption (32-bit or 64-bit) that your computer uses.

</td>
<td headers="Avoid">
**Figure out** the type of encryption (32-bit or 64-bit) that your computer uses.

</td>
</tr>
<tr>
<td headers="Use">
**Click** the link.

</td>
<td headers="Avoid">
**Click on** the link.

</td>
</tr>
<tr>
<td headers="Use">
You can safely **back up a database** by using Cloud Provider Snapshots.

</td>
<td headers="Avoid">
You can safely **back a database up** by using Cloud Provider Snapshots.

</td>
</tr>
</table>

## Don't Use Verbs as Nouns or Adjectives

If a word is defined in the dictionary as a verb, don't use it as a noun or adjective. Some verbs that are commonly misused as nouns or adjectives are *configure*, *compile*, *debug*, and *install*.

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
After **installation** is completed, you can **configure** the product.

</td>
<td headers="Incorrect">
When you complete the **install**, you can begin the **configure**.

</td>
</tr>
<tr>
<td headers="Correct">
After `rubygems` **is compiled**, the following message appears at the bottom of the output text.

</td>
<td headers="Incorrect">
When the **compile process** is finished, the following message appears at the bottom of the output text.

</td>
</tr>
</table>

## Don't Use Non-Verbs as Verbs

Don't use nouns or adjectives as verbs. Don't add verb suffixes to abbreviations, nouns, or conjunctions.

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
You can **reorganize** the table space.

</td>
<td headers="Incorrect">
You can **REORG** the table space.

</td>
</tr>
<tr>
<td headers="Correct">
Verify the change **by using the ping command** to contact the server.

</td>
<td headers="Incorrect">
Verify the change **by pinging** the server.

</td>
</tr>
<tr>
<td headers="Correct">
Some databases and search engines **insert the AND operator** between adjacent words in a keyword search.

</td>
<td headers="Incorrect">
Some databases and search engines **AND** adjacent words in a keyword search.

</td>
</tr>
<tr>
<td headers="Correct">
**Navigate** to the new directory.

</td>
<td headers="Incorrect">
**CD** to the new directory.

</td>
</tr>
</table>

## Use Transitive Verbs Transitively, not Intransitively

Transitive verbs, such as *display* and *complete*, require a direct object. Intransitive verbs don't require a direct object. Be sure to use each type of verb correctly.

To avoid using a transitive verb intransitively, you can make it passive if the performer of the action is understood or not important.

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
The product **displays** the available servers in the right pane. *or* The available servers **are displayed** in the right pane.

</td>
<td headers="Incorrect">
The available servers **display** in the right pane.

</td>
</tr>
<tr>
<td headers="Correct">
After the installation **is completed**, ensure that the FTP services are running.

</td>
<td headers="Incorrect">
After the installation **completes**, ensure that the FTP services are running.

</td>
</tr>
</table>

## Use Correct Plurality Agreements

Verbs have singular and plural forms. Use the verb form that agrees with the subject of the sentence in number.

<table>
<tr>
<th id="When%20the%20subject%20is">
When the subject is

</th>
<th id="The%20verb%20is">
The verb is

</th>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="When%20the%20subject%20is">
A group of things

</td>
<td headers="The%20verb%20is">
Singular

</td>
<td headers="Examples">
A variety of games is available from the App Store.

</td>
</tr>
<tr>
<td headers="When%20the%20subject%20is">
Two or more singular things connected by *and*

</td>
<td headers="The%20verb%20is">
Plural

</td>
<td headers="Examples">
Facebook and Twitter are available from the App Store.

</td>
</tr>
<tr>
<td headers="When%20the%20subject%20is">
Two or more singular things connected by *or*

</td>
<td headers="The%20verb%20is">
Singular

</td>
<td headers="Examples">
Your tablet or phone is all you need to play your favorite games on the go.

</td>
</tr>
<tr>
<td headers="When%20the%20subject%20is">
A singular thing and a plural thing connected by *or*

</td>
<td headers="The%20verb%20is">
Singular or plural, to match the closest subject

</td>
<td headers="Examples">
Skype or social media apps are available from the App Store. Social media apps or Skype is available from the App Store.

</td>
</tr>
</table>

## Don't Humanize Inanimate Objects

Be careful not to ascribe human feelings, motivations, and actions to inanimate objects. For example, a web application doesn't *know*, *need*, *remember*, *see*, *think*, *understand*, or *want*.

Often, we humanize technology with anthropomorphic words. Some writers believe this makes difficult topics more understandable or relatable. These words can make the concept harder to grasp for: - Readers that are less familiar with metaphors. - Readers with English as a second language.

There are standard anthropomorphic verbs in the computer industry. For example, a software program can detect, record, require, store, check, calculate, process, accept, calculate, deny, detect, interact, interpret, listen, refuse, read, and write. You can use anthropomorphic phrases standard to the industry to avoid awkward sentence constructions, but take the time to question common usage and decide if there’s a better word.

In general, avoid phrases that convey **intention** or **desire** (such as *needs* or *wants*), intellect (*thinks*, *knows*, or *realizes*), or emotion (*likes* or *cares*).

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
When you reference your modules in your script by using a PHP function like `include()` or `require()`, the server **can find** them.

</td>
<td headers="Avoid">
When you reference your modules in your script by using a PHP function like `include()` or `require()`, the server **knows where to look for** them.

</td>
</tr>
<tr>
<td headers="Use">
Mission-critical web-based applications and workloads **require** an HA solution.

</td>
<td headers="Avoid">
Mission-critical web-based applications and workloads **need** an HA solution.

</td>
</tr>
<tr>
<td headers="Use">
The software **stores** your security profile and uses it the next time you log in.

</td>
<td headers="Avoid">
The software **remembers** your security profile and uses it the next time you log in.

</td>
</tr>
</table>