---
title: "VBoxManage: Invalid Argument"
date: 2021-04-12T23:26:09-07:00
draft: true
---

## Sample Error Message

```
There was an error while executing `VBoxManage`, a CLI used by Vagrant
for controlling VirtualBox. The command and stderr is shown below.

Command: ["import", "/home/pneuma/.vagrant.d/boxes/csc422-VAGRANTSLASH-testing/20210315.0.1/virtualbox/box.ovf", "--vsys", "0", "--vmname", "output-lubuntu_source_1615876195674_35222_1620240291103_96682", "--vsys", "0", "--unit", "14", "--disk", "/home/pneuma/VirtualBox VMs/output-lubuntu_source_1615876195674_35222_1620240291103_96682/box-disk001.vmdk"]

Stderr: 0%...10%...20%...30%...40%...50%...60%...70%...80%...90%...100%
Interpreting /home/pneuma/.vagrant.d/boxes/csc422-VAGRANTSLASH-testing/20210315.0.1/virtualbox/box.ovf...
OK.
0%...10%...20%...
Progress state: NS_ERROR_INVALID_ARG
VBoxManage: error: Appliance import failed
VBoxManage: error: Code NS_ERROR_INVALID_ARG (0x80070057) - Invalid argument value (extended info not available)
VBoxManage: error: Context: "RTEXITCODE handleImportAppliance(HandlerArg*)" at line 1119 of file VBoxManageAppliance.cpp
```

## Cause

The cause of this error currently unknown.
However, it is likely due to the disk storing the VMs being full (this usually occurs while trying to run `vagrant up`).

## Resolution/Workaround Procedure

Clear up some disk space, and re-run the command that resulted in the error.
Alternatively [set a new storage location for new and/or existing VMs]({{< relref "/faq/storage-location" >}}).
