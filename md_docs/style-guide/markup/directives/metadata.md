---
title: Page Metadata Directives
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup/directives/metadata/
---

# Page Metadata Directives

## meta

Use `.. meta::` to add HTML (Hypertext Markup Language) `<meta>` tags to a page. These tags provide other systems, such as web browsers, search engines, and other web services, with information about the page.

You can specify the `keywords` and `description` name attributes, which can help indexing pages on internal and external search engines. To learn more, see Search Engine Optimization Guidelines.

Use the meta keyword tag standards defined in the Taxonomy tagging instructions.

```rst
.. meta::
   :keywords: read concern, local read concern, read isolation, transactions, multi-document transactions
   :description: You can tune the consistency and availability of your application using write concerns and read concerns.
```

Add the `.. meta::` directive on the line below the page title with a line break in between.

Learn more about the `meta` directive from the Docutils documentation.

## title

Overrides the document title.

```rst
.. title::
```

Learn more about the `title` directive from the Docutils documentation.

## facet

Adds a taxonomy value of product, programming language, or genre.

```rst
.. facet::
```

Learn more about the `facet` directive from the Taxonomy tagging instructions.