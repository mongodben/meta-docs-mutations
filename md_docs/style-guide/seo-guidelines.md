---
title: Search Engine Optimization Guidelines
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/seo-guidelines/
---

# Search Engine Optimization Guidelines

Search Engine Optimization (SEO) considers the actual terms that users enter into search engines (keywords) and employs best practices to improve traffic to web pages from search engines.  Close attention to page metadata and keywords in the page content can improve page placement in search results.  The following guidance helps you to optimize your documentation pages for search.

In addition to this guidance, our content taxonomy improves findability and increases relevance for search queries. To learn more about the instructions and best practices for our content taxonomy, see the Taxonomy tagging instructions.

## Keywords

You can add the actual terms that users enter into search engines (keywords) to the body of your page to improve its SEO.  Google Search Console provides details about the keywords our users enter and you can request this information from the IA and SEO teams.

This guidance makes a distinction between the terms "keywords" and "keyword meta tags". Here "keywords" are popular search terms added throughout the content body, and "keyword meta tags" are metadata specified with the `.. meta::` directive. While "keyword meta tags" are available, some search engines might ignore these tags. To learn more about "keyword meta tags", see Page Metadata Directives. We primaily use "keyword meta tags" to supplement our taxonomy. To learn more about the instructions and best practices for "keyword meta tags", see the Taxonomy tagging instructions.

Add keywords throughout the page copy according to the following best practices:

- Take the most concise form of the information that the page conveys and make that the target keyword.

- Avoid keywords so broad that they compete with the product page.

- Avoid keywords so specific that we miss the actual behavior of our searchers.

If the terms that people search for to try to find a page are "MongoDB Atlas Course", add that phrase in at least one spot. For example, use "This MongoDB Atlas course..." instead of "This Getting Started with Atlas course...".

## Titles

Use the following SEO best practices for page and subsection titles:

- Use a maximum of 70 characters.

- Include target keywords (the most concise form of the information that the page conveys).

- Avoid excessive or irrelevant words (keyword stuffing).

- Use unique page titles. Identical titles, even between documentation sets, compete in search results.

- Don't include "MongoDB" in a title unless the page is a product landing page.

To learn more, see Titles and Headings.

## Alternative Text

Screen readers read alternative text for images aloud so that users can better understand an image. Specify alternative text according to the following SEO best practices:

- Use a maximum of 125 characters per image.

- Describe the image with sufficient detail to understand what it shows.

- If they apply to the image, include keywords (the actual terms that users enter into search engines).

To learn more, see Write for Accessibility.

## Descriptions

The description is a snippet that appears under the link in the search results and is essential for SEO. Write these descriptions according to the following best practices:

- Use a concise description of the page content that is enticing, if possible.

- Emphasize the "why" for using the page.

- Use a maximum of 155 characters.

- Include target keywords and a call to action (CTA) that prompts the user to complete their desired task.

  The following examples use a CTA in the description meta tag:

  ```rst
  .. meta::
     :description: Use a language analyzer to create search keywords in your Atlas Search index that are optimized for a particular natural language.
  ```

  ```rst
  .. meta::
     :description: Use the character filters in an Atlas Search custom analyzer to examine text one character at a time and perform filtering operations.
  ```

- Use unique descriptions for every page.

To learn more, see Page Metadata Directives.