# Slate Linux

Slate is a lightweight Linux distribution built around musl, sinit, and a custom package manager. 

### Table Of Contents

- [System overview](./system.md)
- [Boot process and initramfs](./boot.md)
- [Init system](./init.md)
- [Services](./services.md)
- [Networking](./networking.md)
- [System configuration](./configuration.md)
- [Package manager](./package-manager.md)
- [Ports layout](./ports-layout.md)
- [Creating and maintaining ports](./ports.md)
- [Building software](./building.md)
- [Installation](./installation.md)
- [Troubleshooting](./troubleshooting.md)

## Features

- musl libc
- Custom package manager
- Source-based ports collection
- Minimal default installation
- X11 support
- Lightweight software selection
- Cross-compilation support

## Package Management

Slate uses its own package manager to install and manage software.

### Commands

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

## Configuration
The slate package manager is configured /etc/slate.conf/repos


A git url and a release tag is required; if you want to use the most recent commit set it to testing
## Ports

Slate uses a ports collection to build software from source.

Ports are stored under /usr/ports and organized into categories.

Each package has its own directory containing a port.sh script.

### Categories

- dev: Development tools
- lib: Libraries
- meta: Package collections
- misc: Miscellaneous software
- net: Networking software
- perl: Perl modules
- system: System utilities
- utils: General utilities
- x11: X11 software

## System

Slate uses musl as its C library and sinit for system initialization.

The system is intentionally minimal. Software and services are provided without requiring everything to be installed or enabled by default.

### Services

Service scripts are located in /etc/init.d.

This directory contains both core system services and optional services.

Examples include:
- sdhcp
- filesystems
- seatd
- sshd

Services are managed through their individual scripts.

This documentation describes Slate Linux and its 0.6 development direction.
