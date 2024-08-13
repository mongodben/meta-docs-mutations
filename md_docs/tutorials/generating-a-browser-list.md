---
title: Generating a Browser Coverage List
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/tutorials/generating-a-browser-list/
---

# Generating a Browser Coverage List

While the MongoDB frontend stack is increasingly making use of new and nonstandard Web platform features (such as ES6 modules and candidate ES7 language features), a significant chunk of our users are not using evergreen browsers that are required for these features.

For this reason, we compile our JavaScript and CSS into a form that these older browsers support. However, we want to take a data-driven approach to choosing which older browsers to support using browserslist-ga.

## Prerequisites

Ensure that you have a current version of Node.js, and run the following to install `browserslist-ga` and `browserslist`:

```sh
npm install -g browserslist-ga browserslist
```

## Generate a Stats File

Run the following to generate a browserslist statistics file:

```sh
browserslist-ga
```

This will open a Google authentication workflow in your default browser. Sign in, and return to your terminal to provide the following answers:

<table>

<tr>
<td>
Please select an account:

</td>
<td>
`All MongoDB (#7301842)`

</td>
</tr>
<tr>
<td>
Please select a property:

</td>
<td>
`Combined Traffic (#UA-7301842-14)`

</td>
</tr>
<tr>
<td>
Please select a profile:

</td>
<td>
`Docs - Domain Only (#72085910)`

</td>
</tr>
<tr>
<td>
Specify a start date:

</td>
<td>
Default is 90 days prior

</td>
</tr>
<tr>
<td>
Specify an end date:

</td>
<td>
Default is today

</td>
</tr>
</table>After a moment, `browserslist-ga` should return and write a file called `browserslist-stats.json` that you will provide to `browserslist`.

## Generate a Browser Coverage List

In the same directory, run the following to return a list of browsers that provide 99.5% coverage of docs visitors:

```sh
browserslist --stats=browserslist-stats.json 'cover 99.5% in my stats'
```