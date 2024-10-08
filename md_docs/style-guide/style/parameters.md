---
title: Parameters
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/parameters/
---

# Parameters

This page needs updated content and examples for MongoDB. Though incomplete, this page contains useful information and should be considered a resource though it is under revision.

When documenting parameters, use the following guidelines:

- In request and response examples, show all of the parameters.

- Describe all of the parameters in tables preceding the examples. Use the following guidelines for writing descriptions:

  - Provide meaningful information about the parameter; don't just repeat the parameter's name. Link to other sections of the documentation if more explanation is needed or if the list of possible values is long.

  - Write the first sentence of a description with an implied subject. For example, if the parameter is `name`, the description might be "Server name, which becomes the initial host name of the server."

  - Include any valid values and default value at the end of the description. Use the formats "Valid values are *n* and *n*." and "The default is *n*." For example, "Valid values are `true` and `false`." and "The default is `false`."

- For request body parameters only, label the required parameters by adding the *(Required)* qualifier to the beginning of the description. For example:

  *(Required)* Path of the parameter to update. Valid values are `/enabled`, `/vault/region`, `/vault/use_internal`, and `/log-level`.

  Don't label optional request body parameters. Also, don't label URI, query, or response body parameters as either optional or required.

- When listing and describing request and response body parameters in tables, show the parameters in the same order as they're shown in the examples. If you have more than one example, match the order in the first example shown.

- Format parameter names in text according to the guidelines in Text Formatting.