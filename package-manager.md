# Slate Package Manager

Slate uses its own package manager to install, remove, search, and manage software.

## Commands

Install a package:

    slate install <category>/<package>

Remove a package:

    slate remove <category>/<package>

List installed packages:

    slate installed
 
Update Slate Version:

    slate update

List categories (or packages in a category):

    slate list [<category>]

## Package Names

Packages use category/package identifiers.

Example:

    slate install lib/zlib
    slate install net/curl
    slate install x11/dillo

## Meta Packages

The meta category contains collections of related packages.

## Repositories

Slate 0.6 introduces multiple repository support.

Repository configuration is stored in /etc/slate.conf/repos.

## Package Management Notes

- Use complete package identifiers.
- Check dependencies before installation.
- Review repository configuration.
- Test package removal.
