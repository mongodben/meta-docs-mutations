---
title: Release Notes Guidelines
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/release-notes-guidelines/
---

# Release Notes Guidelines

This page provides general guidance and examples for Release Notes. Verify the correct and consistent guidelines for each product with your team.

Follow the Rackspace Release Guidelines from the Rackspace Style Guide.

For an example that illustrates most of these guidelines, see the Ops Manager Server Release Notes.

## Structure

### Initial Major Version Release

For each major version-specific release note file that you create, observe the following guidelines:

- Use one of the following formats for the title of the release note:

  <table>
  <tr>
  <th id="Format">
  Format

  </th>
  <th id="Example">
  Example

  </th>
  </tr>
  <tr>
  <td headers="Format">
  If the release has a version number, use that in the title.

  </td>
  <td headers="Example">
  ```rst
  .. _opsmgr-server-4.0.13:

  |onprem| Server 4.0.13
  ~~~~~~~~~~~~~~~~~~~~~~

  *Released on 2019-07-04*

  - Removing whitelist from Admin (General > Users) now possible.
    Displays error message when Authentication expires

  - **Agent Upgrades:** :ref:`automation-5.4.20.5541`,
    :ref:`backup-6.8.7.1024`
  ```

  </td>
  </tr>
  <tr>
  <td headers="Format">
  If the release does not have a version number, use the API contract version and date.

  </td>
  <td headers="Example">
  **API | contract version | updates, January 07, 2017**

  </td>
  </tr>
  <tr>
  <td headers="Format">
  If you are documenting a named or initial release, indicate the initial release in the title.

  You can precede release with a type, such as EA or UA.

  </td>
  <td headers="Example">
  **API |contract version | release, September 14, 2017**

  **API |contract version | EA release, September 14, 2017**

  </td>
  </tr>
  </table>

- Use the following main sections in the release notes:

  - What's new

  - Resolved issues

  - Known issues

  - Documentation changes

  Anything previously labeled as "enhancements" can be included either in "What's new" or "Resolved issues" as appropriate.

- Include the "What's new," "Resolved issues," and "Known issues" sections in every RN file, even if you have no content for one of those sections. If one of these sections has no content for a release, use the |no changes| variable for the body text. This variable inserts the boilerplate text "None for this release." For example:

  ```rst
  Known issues
  ````````````

  ``|no changes|``
  ```

- Include the "Documentation changes" section only if you have significant content changes, such as adding an extended example, a tutorial, or new content. If you have no significant content changes for a release, omit that section entirely.

- Order your RN files from latest to earliest, so that the latest is always "on top." For example, the release notes for version 1.1 should precede the release notes for version 1.0 in the hierarchy.

### Formatting

- Use sentence-style capitalization for all headings, including the title of the file (see the examples in the preceding section). The only exception to this rule is the high-level title of the release notes section, which is **Release Notes**.

- If a section has several items, for example there are several resolved issues to document, provide the descriptions in a bullet list. You do not need to precede the bullet list with an introductory sentence, unless one is necessary for clarity.

- If you have only one item to document in a section, do not show it as a bullet item. Show it as regular text.

- Use the punctuation guidelines for lists at List Items.

- As needed, use the guidelines at Text Formatting.

### Wording

You do not need to include an introductory paragraph for each file. The one that exists for the "Release Notes" section as a whole is sufficient. You can begin each file with the "What's new" heading. However, you can include an introductory paragraph if necessary—for example, if you want to state that the release notes correspond to a particular type of release, such as a Limited Availability release, or you need to introduce the first release of a major version.

If you refer to content in another part of the API document, provide a link to the specific section.

Use the following guideline when creating items in each section:

<table>
<tr>
<th id="Section">
Section

</th>
<th id="Guideline">
Guideline

</th>
<th id="Examples">
Examples

</th>
</tr>
<tr>
<td headers="Section">
What's new

</td>
<td headers="Guideline">
Use sentences to describe the new feature or enhancement. Provide as needed, and provide a link to any section in the documentation that describes that feature.

</td>
<td headers="Examples">
Supports IPv6. When you create a server, you can specify both IPv4 and IPv6 addresses.

</td>
</tr>
<tr>
<td headers="Section">
Resolved issues

</td>
<td headers="Guideline">
Provide an initial phrase that describes the issue that was fixed. Start the phrase with a verb. Use present tense or past tense consistently throughout the release notes. If necessary, include sentences to further explain the fix and the previous behavior. If you list only phrases, do not use ending punctuation.

</td>
<td headers="Examples">
- Supports Debian 8 (Jessie).

- Trims the Monitoring ID and Monitoring Token configuration variables to ensure correctness.

- Fixes the Xen Server 6 package repository to resolve an issue that caused inconsistencies and errors with package management.

</td>
</tr>
<tr>
<td headers="Section">
Known issues

</td>
<td headers="Guideline">
Use sentences to describe the issue. If a workaround is available, explain it.

</td>
<td headers="Examples">
Results from the `$indexStats` operator exclude queries that use the `$match` or `mapReduce` functions.

</td>
</tr>
<tr>
<td headers="Section">
Documentation changes

</td>
<td headers="Guideline">
Provide an initial phrase that describes the issue that was fixed. Start the phrase with a verb. Use present tense or past tense consistently throughout the release notes. If necessary, include sentences to further explain the changes. If you list only phrases, omit ending punctuation. Provide a link to the relevant section in the documentation.

</td>
<td headers="Examples">
Clarifies the alert policy descriptions to include how the polling window affects the alarm state. To learn more, see /alerts/.

</td>
</tr>
</table>

### Editing Existing Release Notes

In cases where existing release notes were not accurate at the time of publication, change the content to make it accurate. You can make the following types of changes:

- Fix typos

- Correct links that were wrong at the time of publication

- Correct incorrect statements to reflect what was correct at the time of publication