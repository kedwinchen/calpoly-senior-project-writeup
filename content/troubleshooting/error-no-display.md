---
title: "Error: no DISPLAY environment variable specified"
date: 2021-04-12T23:26:28-07:00
draft: true
---

## Sample Error Message

```
Error: no DISPLAY environment variable specified
```

## Cause

This is (usually) caused by attempting to run a graphical application through X forwarding (over `vagrant ssh`), but no X server is installed.
This is to be expected on non-Linux (i.e., Windows (and macOS)) operating systems.

## Resolution/Workaround Procedure

To use a graphical application, use the VirtualBox GUI directly to get direct (graphical) console access.

{{< hint "info">}}
By default, the username/password for Virtual Machines managed by Vagrant is `vagrant` (for both the username and password).
{{< /hint >}}

<!-- TODO: write something about MobaXTerm and other terminal emulators with built-in X servers (needs testing first) -->
