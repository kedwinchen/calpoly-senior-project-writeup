---
title: "Network Interface"
date: 2021-04-23T11:02:06-07:00
draft: true
---

## Example Error Message

```
There was an error while executing `VBoxManage`, a CLI used by Vagrant for controlling VirtualBox.

The command and stderr is shown below.
Command: ["startvm", "979bcfeb-8860-41b3-a513-ee2da299a1ca", "--type", "headless"]

Stderr:
VBoxManage.exe: error: Failed to open/create the internal network 'HostInterfaceNetworking-VirtualBox Host-Only Ethernet Adapter #3' (VERR_INTNET_FLT_IF_NOT_FOUND).
VBoxManage.exe: error: Failed to attach the network LUN (VERR_INTNET_FLT_IF_NOT_FOUND) VBoxManage.exe: error: Details: code E_FAIL (0x80004005), component ConsoleWrap, interface IConsole
```

## Cause

The cause of this error is currently unknown

## Resolution/Workaround Procedure

### Manually Connect the Adapter

0. Open a terminal, and navigate to the directory with the Vagrantfile
1. Shut down the VM (`vagrant halt <vm name>`)
2. Open VirtualBox Manager GUI
3. Open the `Settings` window of the VM that is causing the error
4. In the `Network` section, select the tab with the Ethernet Adapter that is causing issues (in the example above, the tab would be the one with the adapter connected to `VirtualBox Host-only Ethernet Adapter #3`)
5. Change the `Attached to` value from the set value to `Not Connected`
6. Click `OK` and close the `Settings` window
7. Start the VM (using `vagrant up <vm name>`)
8. After the VM has booted successfully, open the `Settings` window of the VM
9. In the `Network` section, select the tab modified in step 5.
10. Change the `Attached to` value from the set value to `Host-only Adapter` (or the correct type from before)
11. If needed, change the value `Name` field to the desired network
12. Without shutting down the VM, run `vagrant provision`
