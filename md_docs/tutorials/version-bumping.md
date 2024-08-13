---
title: Version Bumping
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/tutorials/version-bumping/
---

# Version Bumping

## Introduction

Periodically the documentation team must document a new product version. The process broadly follows these steps:

- Create a branch for the previous version, leaving `master` as the branch for the new release.

- Update the `config/build_conf.yaml` file's `version.release` key to the new version.

- In the `docs-tools` repository under the `data/` directory, update the project's published branches configuration file.

- Update the redirects configuration file.

- Publish all branches.

## Tutorial

Consider a hypothetical project called `bi-connector`. This product is currently on version 2.2, but documentation work must begin for version 2.3.

As part of this release, the `tutorial/connecting-to-atlas` path has been removed, and users should be redirected to `reference/mongosqld`.

### Step 1: Branch

From the project's repository, create a new branch for the current version:

```sh
git checkout -b v2.2 upstream/master
git pull --rebase
git push origin v2.2
git checkout master
```

### Step 2: Update project version

In the `bi-connector` repository under the `config/` directory, you will find a file called  `build_conf.yaml`. Update this file's `version.release` key to `2.3`:

```yaml
version:
  release: '2.3'
  branch: 'master'
```

### Step 3: Update published branches configuration

- Create a new local branch in the `docs-tools` repository:

  ```sh
  git checkout -B bi-v2.3 upstream/master
  git pull --rebase
  ```

- Navigate to the `data/` directory and open the file named `bi-connector-published-branches.yaml`.

- Update this file to include a `2.3` version and a `v2.2` branch; and set the `version.upcoming` key to `2.3`.

- Commit your change and push the commit to origin <local branch>.

- Create a separate PR to merge the change to master.

<table>
<tr>
<th id="Before">
Before

</th>
<th id="After">
After

</th>
</tr>
<tr>
<td headers="Before">
```yaml
version:
  published:

    - '2.2'
    - '2.1'
    - '2.0'
    - '1.1'
  active:

    - '2.2'
    - '2.1'
    - '2.0'
    - '1.1'
  stable: '2.2'
  upcoming:
git:
  branches:
    manual: 'master'
    published:
      - 'master'

      - 'v2.1'
      - 'v2.0'
      - 'v1.1'
...
```

</td>
<td headers="After">
```yaml
version:
  published:
    - '2.3'
    - '2.2'
    - '2.1'
    - '2.0'
    - '1.1'
  active:
    - '2.3'
    - '2.2'
    - '2.1'
    - '2.0'
    - '1.1'
  stable: '2.2'
  upcoming: '2.3'
git:
  branches:
    manual: 'master'
    published:
      - 'master'
      - 'v2.2'
      - 'v2.1'
      - 'v2.0'
      - 'v1.1'
...
```

</td>
</tr>
</table>

### Step 4: Update redirects configuration

In the `bi-connector` repository under the `config/` directory, you will find a file called  `redirects`. Update this file accordingly:

- Add `v2.2` to the `versions` list,

- Add an `upcoming` symlink,

- Add a `v2.3` symlink so that users can refer to `master`, `upcoming`, and `v2.3` interchangeably,

- Update the `current` symlink to point to `v2.2`, and

- Add a redirect for the removed file.

```none
define: prefix bi-connector
define: base https://www.mongodb.com/docs/${prefix}
define: versions v1.1 v2.0 v2.1 master
symlink: v2.2 -> master
symlink: current -> master
```

```none
define: prefix bi-connector
define: base https://www.mongodb.com/docs/${prefix}
define: versions v1.1 v2.0 v2.1 v2.2 master
symlink: v2.3 -> master
symlink: upcoming -> master
symlink: current -> v2.2

[v2.3-*]: ${prefix}/${version}/tutorial/connecting-to-atlas -> ${base}/${version}/reference/mongosqld
```

Redirects for details on the redirects format.

### Step 5: Redeploy

- Wipe your `build` directory. Sphinx will not properly rebuild files to include changes to the version selector.

- Run `make publish` on the `master` branch first. This ensures that `mut-redirects` creates symbolic links under `build/public` for future builds.

- Run `make-publish` on each branch, going from oldest to newest. For each branch, check the output's version selector to make sure that the version selector looks correct, and then run `make deploy`.