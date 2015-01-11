# Fonts-Roboto-Slab

Font Roboto Slab is a Roboto font family

## Disclaimer

This is not an official package from Google.

Current version: 1.0

<!--
TODO: Add a getting started section for running from a pre-built binary.
-->

## Prerequisites

Building requires command `dpkg-buildpackage` and `dh_make`. You must install `git` to clone source or get it via HTTPS

## Building the source code

If you are newbie, this is guide for quick build.

First checkout the code from the git repo:

    git clone git@github.com:ansidev/fonts-roboto-slab.git

Build the binary:

Change to directory fonts-roboto-slab-1.0

    cd fonts-roboto-slab-1.0

And then generate file fonts-roboto-slab_{$VERSION}.orig.tar.xz:

    dh_make --createorig

Start build package:

    dpkg-buildpackage -uc -us -b

Finally, test package:

    lintian ../fonts-roboto-slab_{$VERSION}_all.deb

## Install package into the Ubuntu/Debian system

    sudo dpkg -i ../fonts-roboto-slab_{$VERSION}_all.deb
