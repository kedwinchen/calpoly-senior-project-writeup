---
title: "Could not open the medium"
date: 2021-05-05T11:23:33-07:00
draft: true
---

## Sample Error Message

```
There was an error while executing `VBoxManage`, a CLI used by Vagrant
for controlling VirtualBox. The command and stderr is shown below.

Command: ["startvm", "e02c85e6-433d-4274-8089-13aacac79808", "--type", "headless"]

Stderr: VBoxManage: error: Could not open the medium '/path/to/box-disk001.vmdk'.
VBoxManage: error: VMDK: inconsistency between grain table and backup grain table in '/path/to/box-disk001.vmdk' (VERR_VD_VMDK_INVALID_HEADER).
VBoxManage: error: VD: error VERR_VD_VMDK_INVALID_HEADER opening image file '/path/to/box-disk001.vmdk' (VERR_VD_VMDK_INVALID_HEADER)
VBoxManage: error: Details: code NS_ERROR_FAILURE (0x80004005), component MediumWrap, interface IMedium
```

## Cause

The cause of this error is likely due to the disk storing the VMs being full (this usually occurs while trying to run `vagrant up`).

## Resolution/Workaround Procedure

Clear up some disk space, and re-run the command that resulted in the error.
Alternatively [set a new storage location for new and/or existing VMs]({{< relref "/faq/storage-location" >}}).
