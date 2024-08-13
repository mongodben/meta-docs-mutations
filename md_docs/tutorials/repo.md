---
title: How to Create a Docstools-Enabled Repository
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/tutorials/repo/
---

# How to Create a Docstools-Enabled Repository

In this guide you will learn how to create a docstools-enabled repository.

*Time required: 45 minutes*

## Prerequisites

- Access to git

## Check Your Environment

- Check to make sure you have git installed

## Procedure

### Clone a repo similar to the repository you wish to create.

First, clone a repository that is similar to the repository you wish to create.

For this example, we will clone the docs-meta repository. Clone the repo to the name you wish to give your new repo.

```sh
git clone git@github.com:mongodb/docs-meta.git <docs-yourrepo>
```

Run:

```sh
cd <docs-yourrepo>
```

### Delete the .git directory

Delete the .git directory in your local, cloned version of the repository so that you can begin with your own repository.

```sh
rm -rf .git
```

Check to make sure you have deleted the .git file:

```sh
git branch
```

You should see the following error:

```sh
fatal: Not a git repository (or any of the parent directories): .git
```

### Check to make sure you have removed the .git directory

Before you proceed, check to make sure that .git directory is gone by running ls:

```sh
ls -al
```

Your output should be something like:

```sh
total 32
drwxr-xr-x   7 you  staff   238 Mar 11 05:05 .
drwxr-xr-x  85 you  staff  2890 Mar 11 05:02 ..
-rw-r--r--   1 you  staff  2424 Mar 11 05:02 .gitignore
-rw-r--r--   1 you  staff  2243 Mar 11 05:02 Makefile
-rw-r--r--   1 you  staff  7087 Mar 11 05:02 conf.py
drwxr-xr-x   8 you  staff   272 Mar 11 05:02 config
drwxr-xr-x  17 you  staff   578 Mar 11 05:02 source
```

### Reinitialize the repo

Run git init to reinitialize the repo:

```sh
git init
```

You will see the following output:

```sh
Initialized empty Git repository in <yourdirectorystructure>/docs-yourrepo/.git/
```

Check your work:

```sh
ls -al
```

The new .git directory should now appear.

### Create the repository on GitHub

Create the repo you would like to use on GitHub.

You will then need to commit some files and add your local repository to github. If you add all of the files, you will need to remove the ones that are not relevant to your repository later, but this is a perfectly acceptable way to start your repository.

Make sure you add a README.md file to your repo. Add a sentence to the file to describe your project. Then save the file and run:

```sh
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:mongodb/docs-yourrepo.git
git push -u origin master
```

### Fork the repo

Go ahead and fork the repo on github if you wish to follow the docs model of github usage. Fork a repo.

This is not a requirement if your team follows a different workflow. If you wish to branch off the root repository, skip this step entirely.

Add the origin remote for your forked repo:

```sh
git remote add origin https://github.com/<fork>/docs-yourrepo
```

Add the upstream remote:

```sh
git remote add upstream https://github.com/<repoOwner>/<remoteRepoRoot>.git
```

### Remove the redirects file

Some of our repositories have a `redirects` file that redirects browsers permanently to a new location.

Please remove the file in order to prevent inadvertant redirects on your site.

In the config directory of your repo, run:

```sh
rm redirects
```

### Edit conf.py

Edit the conf.py as needed. `conf.py` is where you can add sphinx extensions and roles that you might require for your docs.

If you'd like to accept the default `conf.py`, that's fine too.

### Edit config/sphinx_local.yaml

In this `config/sphinx_local.yaml` file, you will want to change the name of the project:

```sh
project: 'mongodb-<yoursitename>'
```

### Edit config/build_conf.yaml

In order to make sure that your builds go to the right location on staging and production, modify the `config/build_conf.yaml` file.

- Modify the git/remote section to reflect your repository.

- Modify the project name to match the name of your project.

- Modify the url and tag in the project section.

```sh
git:
  remote:
    upstream: 'mongodb/docs-yourrepo'
    tools: 'mongodb/docs-tools'
project:
  name: 'yourprojectname'
  tag: 'ypt'
  url: 'https://www.mongodb.com/docs/projectname'
  title: 'MongoDB Project Documentation'
  branched: false
```

### Install Build Tools

You will need to install the build tools in order to build your repository.

Once you have installed the build tools, you can attempt to build your repository.

### Running a Build Locally

If you are simply planning to build locally, you can build your repository by running:

```sh
make html
```

You will see output pertaining to your build in the `build/<branch>` directory local to your repository.

## Summary

If you have successfully completed this guide, you have created a MongoDB docstools-enabled repository.

## What's Next

Now that you've created your repository, you can create your docstools-enabled content.

## See Also

- For examples, see the Guides site.

- Tabbed Content Tutorial