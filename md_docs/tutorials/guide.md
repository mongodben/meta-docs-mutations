---
title: How to Create a Guide for MongoDB Docs
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/tutorials/guide/
---

# How to Create a Guide for MongoDB Docs

In this guide, you will create a MongoDB Guide.

*Time required: 45 minutes*

## Prerequisites

- a docs repository that leverages docs-tools

- content for the guide

Check Your Environment:

- check for the conf.py script in your repository root (you'll need this if you want to compile a guide)

## Procedure

### Add guides to your sphinx extensions.

Add `guides` to the extensions list in `conf.py` in your repo root.

```sh
extensions = [
  'sphinx.ext.extlinks',
  'sphinx.ext.todo',
  'mongodb',
  'directives',
  'intermanual',
  'testcode',
  'tabs',
  'markdown',
  'fasthtml',
  'source_constants',
  'icon'
  'guides'
]
```

### Copy the guides directive template into a file in your repo.

Copy the following directive template into a file to begin writing your guide. Make sure it's under the source directory and give it a `.txt` extension. Otherwise it won't build.

While the spacing makes this example look a bit like a `.yaml` file, it's really a Sphinx directive. This guide should compile as-is.

```yaml
.. guide::
   title: This is your guide title
   author: MongoDB Documentation Team
   type: Getting Started
   level: beginner
   product_version: 4.0
   languages:
     shell
     compass
     python
     java-sync
     nodejs
     motor
     csharp
   result_description:
     This is a handy description of the result you will achieve
     if you successfully create this guide.
   time: 15
   prerequisites:
     - first do this guide
     - then do this one
     - make sure you have installed some stuff
   check_your_environment:
     Check to see if your environment has everything it needs.
     List things you need to complete this guide
       - binaries installed
       - permissions
       - drivers or libraries
   procedure:
     Feel free to put the steps include here.

     At the moment, tabbed content does not display properly when
     put directly in the procedure section. Use an include file
     for tabbed content.

   summary:
     Congrats! You accomplished something.
   whats_next:
     - check out the `guide on such and such </guide/such-and-such>`
```

### Fill in your guide template

Now it's time to fill in the fields in the template to create your guide.

The languages section is optional, so use it only if you would like pills at the top of your page and have tabbed language content (`tabs-drivers`) to toggle.

The following sections are required:

<table>
<tr>
<th id="field">
field

</th>
<th id="type">
type

</th>
<th id="possible%20values">
possible values

</th>
</tr>
<tr>
<td headers="field">
title

</td>
<td headers="type">
string

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
author

</td>
<td headers="type">
string

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
level

</td>
<td headers="type">
string

</td>
<td headers="possible%20values">
beginner, intermediate, advanced

</td>
</tr>
<tr>
<td headers="field">
time

</td>
<td headers="type">
number

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
type

</td>
<td headers="type">
string

</td>
<td headers="possible%20values">
Getting Started, Use Case, Deep Dive

</td>
</tr>
<tr>
<td headers="field">
product_version

</td>
<td headers="type">
number

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
prerequisites

</td>
<td headers="type">
text

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
summary

</td>
<td headers="type">
text

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
procedure

</td>
<td headers="type">
text

</td>
<td headers="possible%20values">
any

</td>
</tr>
<tr>
<td headers="field">
result_description

</td>
<td headers="type">
text

</td>
<td headers="possible%20values">
any

</td>
</tr>
</table>

### Document the content with steps required to complete the tutorial

Document the steps required for your guide. If you'd like content with numbered steps, use a step file.

Step files are `.yaml` files that get converted during the build process to `.rst` files and are included as `/<dir>/steps/<something>.rst`. When you create the `.yaml` step file, name it according to the convention:

Guides use headings to delineate sections. If you would like to provide subsections for your guides sections, use subheadings.

```sh
<dir>/steps-<something>.yaml
```

Here is an example of a `.yaml` steps file.

You can nest `include` directives within the `step` content if you wish.

```yaml
title: Find the ``mongo`` Shell
ref: mongo-shell
content: |

  The ``mongo`` shell is packaged with the MongoDB Server
  Community and Enterprise distributions, and is also available
  for users of Atlas as a client-only download.

  If you do not have ``mongo`` shell installed, follow the
  install directions for your environment.

  .. include:: /includes/guides/download-shell-tabs.rst

---

title: Connect to your MongoDB instance
ref: connect
content: |

  .. include:: /includes/guides/mongo-shell-platform-connect-np.rst
```

### Add What's Next and See Also (optional) sections

The **What's Next** and **See Also** sections are important for leading the reader to the next step in their learning.

Add links to other tutorials in the **What's Next** section and save **See Also** for content that links out of the tutorial format such as in-depth manual content and reference material.

If you have `:manual:` in your `conf.py` as an extlink map, you can use:

```sh
:manual:`short description </reference/blah>`
```

Or for content that lives in your own repo, feel free to use:

```sh
:doc:`Some Local Content </localdir/localcontent>`
```

External links or links referenced from outside of a repo with shortcuts configured can be referenced using the fully qualified url:

```sh
`Site to link to <http://fully.qualified.domain/stuff>`__.
```

### Add the Guide to a Table of Contents

To add the guide to a table of contents, use the same method you would use for any standard docs content.

In the `.txt` file for the TOC in question, add the link.

```rst
.. toctree::
   :titlesonly:

   /images-guide
   /style-guide/markup/directives/tabs
   /tutorials/version-bumping
   /tutorials/generating-a-browser-list
   /error-kb
   /tutorials/guide
```

## Summary

If you have successfully completed this guide, you have created a MongoDB guide and added it to your table of contents.

## What's Next

You've reached the end of this one part series on creating guides!

## See Also

- For examples, see the Guides site.

- Tabbed Content Tutorial