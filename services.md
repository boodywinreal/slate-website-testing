# Services

Service scripts are located in `/etc/init.d/`.

This directory contains both core system services and optional services.

Examples include:
- sdhcp
- filesystems
- seatd
- sshd

Services are managed through their individual scripts.

## Listing Services

    ls /etc/init.d

## Running Services

Service scripts are invoked directly.

    /etc/init.d/sshd

Check each script for supported arguments such as start, stop, and restart.

## Service Management

- Only run services that are needed.
- Check configuration before starting services.
- Verify required users and groups exist.
- Check executable permissions.
- Inspect service output when troubleshooting.

A service being installed does not mean it must be running.
