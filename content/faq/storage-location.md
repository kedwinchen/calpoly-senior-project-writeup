---
title: "How do I change the storage location for VM files?"
date: 2021-04-05T22:25:06-07:00
draft: true
---

Please note that the storage location for VMs is not (currently) managed by Vagrant. It is managed by VirtualBox.

There are a few options (see Table of Contents in right)

## Change default storage location for NEW VMs

### Using the Graphical User Interface

1. Open VirtualBox Manager
2. File -> Preferences
3. Under "General", modify the "Default Machine Folder"
4. **_NEW VMs_** will be created there (existing VMs are **_NOT_** affected)

### Using the Command Line Interface

Run the following command:

{{< tabs "storage-locations-cli" >}}
{{< tab "macOS/Linux" >}}

```shell
vboxmanage setproperty machinefolder /path/where/you/want/new/VirtualBoxVMs
```

{{< /tab >}}
{{< tab "Windows" >}}

Be sure to sepcify the drive letter as well. In this case, the directory is on the `X:` drive.

```powershell
vboxmanage setproperty machinefolder X:\storage\location\of\new\VirtualBoxVMs
```

{{< /tab >}}
{{< /tabs >}}

## Change storage location for EXISTING VMs

1. Open VirtualBox Manager
2. Right click on the VM to move
3. Select the new folder to move the VM to
