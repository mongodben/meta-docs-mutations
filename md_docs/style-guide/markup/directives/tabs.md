---
title: Tabbed Content
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/markup/directives/tabs/
---

# Tabbed Content

Use the tabbed content directive `tabs` to organize information into a set of tabs.

## Choosing a Tab Set

There are two types of directives in the tabs extension:

- Pre-defined Tab Sets: Used for common groups of tabs that are shared across several pages. Pre-defined tab sets do not require the writer to specify the tab's display name and also provide error and consistency checking.

- Custom Tab Set: Used for a group of tabs that only apply to a single unique page. Custom tab sets are flexible but require the writer to provide the tab's display name and do not offer any error or consistency checking.

### Usage

The following usage guidelines apply to both pre-defined tab sets and custom tab sets:

Use a tabs directive to indicate blocks of dynamic content on a page. Dynamic content is any content on the page that will show or hide depending on the tab selected. There is no limit to the number of tabs directives per page, but if there is more than one they should be of the same type. For example, once `.. tabs-drivers::` is used all tab instances on the page should also be `.. tabs-drivers::`.

The tab directive may be used to display content for a single tab or a small subset of tabs. For example, the tabs directive can be used to display a specific caveat for the Mongo Shell on a drivers page without needing to specify blank stubs for all other languages on the page:

```rst
.. tabs-drivers::
   :hidden:

   .. tab::
      :tabid: shell

      .. note::
         Some caveat about the shell. Don't show anything for
         other languages or make the writer list all other
         languages in this directive instance.
```

When there is only content for a subset of the page's tabs, consider hiding the tabs using `hidden: true`. Otherwise, the directive only renders tabs included in this directive. This might make it seem like tabs are missing and may confuse readers.

### Using a Pre-defined Tab Set

When two or more pages share the same or similar set of tabs, use a pre-defined tab set. Pre-defined tab sets perform the following across all pages that use the same tab set:

- Save the user's preference and automatically apply it when they visit pages using the same tab set

- Ensure tabs appear in the same order

- Eliminate the need for the writer to specify the tab display name (tab label)

To find the pre-defined tab sets, see the Snooty configuration file. Each entry starts with `[directive.tabs-`.

Pre-defined tab sets require the following fields for each tab:

- `id`

- `content`

The following example uses the `tabs-drivers` directive to display code examples stored in different files:

```rst
.. tabs-drivers::

   .. tab::
      :tabid: shell

      .. code-block:: javascript

         db.inventory.find( {} )

   .. tab::
      :tabid: python

      .. literalinclude:: /driver-examples/test_examples.py
         :language: python
         :dedent: 8
         :start-after: Start Example 7
         :end-before: End Example 7

   .. tab::
      :tabid: java-sync

       .. literalinclude:: /driver-examples/DocumentationSamples.java
          :language: java
          :dedent: 8
          :start-after: Start Example 7
          :end-before: End Example 7

   .. tab::
      :tabid: java-async

      .. literalinclude:: /driver-examples/AsyncDocumentationSamples.java
         :language: java
         :dedent: 8
         :start-after: Start Example 7
         :end-before: End Example 7

   .. tab::
      :tabid: nodejs

      .. literalinclude:: /driver-examples/examples_tests.js
         :language: javascript
         :dedent: 8
         :start-after: Start Example 7
         :end-before: End Example 7
```

### Defining a New Tab Set

To learn more about creating a new pre-defined tab set, contact the Docs Platform Team.

### Using a Custom Tab Set

The custom tab set is best suited for unique pages that will not share a similar set of tabs with another page. User preference will be saved on a per page basis when the custom tab set is used.

The custom tab directive requires the following fields for each tab:

- `id`

- `name`

- `content`

The following example uses the custom tabs set to organize information on different types of Ops Manager logs:

```rst
.. tabs::

   .. tab:: Real-Time Logs
      :tabid: realtime

      The Monitoring Agent collects real-time log information...

   .. tab:: On-Disk Logs
      :tabid: ondisk

      Ops Manager can collect on-disk logs...

   .. tab:: Agent Logs
      :tabid: agent

      Ops Manager collects logs for all your Automation Agents...
```

The custom directive does not check for errors or consistency. If the `id` and `name` pairs differ from instance to instance on the same docs page, they will be treated as different tabs.

If there are multiple pages with similar tabs, a pre-defined tab set should be created with these values. For more information, see Defining a New Tab Set.

## Tab Location

### Inline Tabs

Tabs will render inline directly above the tabbed content by default. If you wish to hide the tabs, include `hidden: true` inside your tab directive:

```rst
.. tabs-drivers::
   :hidden:

   .. tab::
      :tabid: shell

      For more information on the syntax of the method, see
      :method:`~db.collection.find()`.

   .. tab::
      :tabid: python

      For more information on the syntax of the method, see
      :py:meth:`~pymongo.collection.Collection.find`.
```

Hiding tabs may be useful for tab directives that only contain text. Too many tab strips run the risk of cluttering the page. Consider the following example with an unnecessary tab strip on text which immediately follows a code block:

**Before Hiding:**

<Tabs>

<Tab name="MongoDB Shell">

```javascript
db.inventory.find( {} )
```

</Tab>

<Tab name="Python">

```python
cursor = db.inventory.find({})
```

</Tab>

</Tabs>

<Tabs>

<Tab name="MongoDB Shell">

For more information on the syntax of the method, see db.collection.find().

</Tab>

<Tab name="Python">

For more information on the syntax of the method, see pymongo.collection.Collection.find.

</Tab>

</Tabs>

**After Hiding:**

<Tabs>

<Tab name="MongoDB Shell">

```javascript
db.inventory.find( {} )
```

</Tab>

<Tab name="Python">

```python
cursor = db.inventory.find({})
```

</Tab>

</Tabs>

<Tabs>

<Tab name="MongoDB Shell">

For more information on the syntax of the method, see db.collection.find().

</Tab>

<Tab name="Python">

For more information on the syntax of the method, see pymongo.collection.Collection.find.

</Tab>

</Tabs>

### Top of the Page

For pages that make immediate use of tabbed content and continue to use tabbed content throughout, consider using a single tab strip near the top of the page.

To render only a single tab strip at the top of the page, include the following directive anywhere on the page:

```sh
.. tabs-top::
```

Ensure all required tabs are present in the first use of tabs. The tab selector at the top of the page is built using the first instance of tabs in the document.