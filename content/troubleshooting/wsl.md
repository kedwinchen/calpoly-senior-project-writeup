---
title: "Windows Subsystem for Linux (WSL)"
date: 2021-04-12T23:27:15-07:00
draft: true
---

## The Situtation

Despite the [official documentation on Microsoft's website](https://docs.microsoft.com/en-us/windows/wsl/compare-versions), <!-- it is a known issue that --> VirtualBox appears to be incompatible with Windows Subsystem for Linux (WSL) (at least with version 2, not tested with version 1).

{{< hint warning >}}
This is true for VirtualBox 6.1 (the current version), WSL versions 1 and 2, and Windows 10 Build 2004.
Compatibility unknown for VirtualBox 6.1 and other Windows 10 versions.
This notice will be removed and/or updated when futher information is available.
{{< /hint >}}

This is due to WSL requiring `Virtual Machine Platform` feature to be enabled.
As such, the current workaround is to temporarily disable the feature by following the following procedures.

## The Workaround

1. Open Control Panel (use the search feature or use `Windows Key + R` (should open the `Run` dialog box), type in `control` and hit `Return (Enter)`)
2. Click on `Programs and Features`
3. On the left side, click `Add or remove Windows features`
4. Uncheck the box for `Virtual Machine Platform` (see note, below)
5. Reboot the computer (save any unsaved work first)

Updated instructions will be posted on this page in the event better solutions are found.

### Note

- you can leave the box for `Windows Subsystem for Linux (WSL)` checked, but WSL will likely be inoperable until `Virtual Machine Platform` is re-enabled
- To re-enable WSL functionality, check follow the procedure above, but check the box for `Virtual Machine Platform`.
  A system reboot will likely be required to re-enable WSL functionality.
