---
layout: post
title:  "Efficiently house cleaning the .pacnew files in Archlinux"
date:   2016-02-28 11:17:27 -0800
categories: archlinux maintenance
---
If you've been using (and updating!) Archlinux for awhile, you may have noticed that your filesystem has become littered with files having the extension `.pacnew`, `.pacsave` and the like. These files are left by pacman when an update requires changes to the configuration files: rather than over-write the existing file (and potentially destroy your local configuration), pacman leaves behind a `.pacnew` file with the new configuration options so that you can merge them in manually.

In many cases it's important not to let these files accumulate. Keeping an Archlinux system on the bleeding edge of software also means being on the bleeding edge of the configurations. Here's my simple work-flow for merging in these files using a few handy tools, and vim.
