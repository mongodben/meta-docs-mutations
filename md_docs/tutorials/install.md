---
title: Installing MongoDB Documentation Build Tools
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/tutorials/install/
---

# Installing MongoDB Documentation Build Tools

In this guide you will learn how to install the MongoDB Documentation Build Tools on macOS.

*Time required: 45 minutes*

## Prerequisites

- macOS 10.14 or later.

## Procedure

### Install Xcode from the App Store.

Install XCode. This installation may take some time.

### Install or link macOS SDK headers.

The following step depends on which version of macOS you are running:

<Tabs>

<Tab name="Mojave">

If you are running macOS Mojave (10.14) or later, install the macOS SDK headers by running the following command:

```sh
open /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg
```

</Tab>

<Tab name="Catalina or later">

Run the following command to manually link the XCode libraries to your local path:

```sh
ln -s '/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/usr/include/libxml2/libxml/' /usr/local/include
```

</Tab>

</Tabs>

### Download and install Homebrew

If Homebrew is not installed, install it:

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

When this completes, run the following commands:

```sh
brew update
brew doctor
```

### Install Python 2 and Python 3

The build tools require Python 3 and 2 *from Homebrew*. The version of Python which comes with macOS is unsupported and will **not** work.

Install Python 2 by running the following commands:

```sh
curl -LO https://raw.githubusercontent.com/Homebrew/homebrew-core/86a44a0a552c673a05f11018459c9f5faae3becc/Formula/python@2.rb

brew unlink openssl && brew install python@2.rb
```

Install Python 3 by running the following command:

```sh
brew install python@3.8
```

### Install Giza

Install Giza, Sphinx, and their dependencies with Python 2:

```sh
python -m pip install -r https://raw.githubusercontent.com/mongodb/docs-tools/master/giza/requirements.txt
```

You might receive the an error containing the following text when you try to install Giza, Sphinx, and their dependencies:

```sh
No module named pip
```

If you receive this error, run the following commands, then try to install Giza, Sphinx, and their dependencies again:

```sh
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py

python get-pip.py
```

### Install Mut

Install Mut and its dependencies with Python 3:

```sh
brew install pkg-config
python3 -m pip install mut
```

### Install Inkscape

First install XQuartz through Homebrew:

```sh
brew install --cask xquartz
```

Once XQuartz is installed, download and install Inkscape.

## Summary

If you have successfully completed this guide, you have installed the MongoDB Build Tools.

## What's Next

Congratulations! Now that you've installed the Build Tools, you are ready to start building your site.

## See Also

- For examples, see the Guides site.

- Tabbed Content Tutorial

- Create a Docstools-Enabled Repo