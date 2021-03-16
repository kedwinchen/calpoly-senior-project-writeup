---
title: "CSC 422: Network and Web Security"
date: 2021-03-15T01:33:12-07:00
draft: true
---

## Vagrantfile

The Vagrantfile is located [here]({{< relref "/" >}}../files/2021-spring/csc/422/Vagrantfile)

To use, [follow the instructions]({{< relref "/instructions/students" >}})


## Special Notices/Instructions

- All VMs except the `router` VM should not be directly connected to the network.
  Even though the NAT adapter is connected, no traffic should leave through that adapter by default.
  Traffic is routed instead to the `router` VM.
- The `router` VM does not route traffic by default. This is intended (it is the first lab assignment, or so I am told).


## System Requirements

- Minimum specifications:

    - RAM (memory): 5 GiB
    - CPU (processor): amd64/x86_64 quad-core (or dual-core with Hyper-Threading)
    - Disk space (hard drive/solid state): 32 GiB free space

- Recommended specifications:

    - RAM (memory): 16 GiB
    - CPU (processor): amd64/x86_64 quad-core with Hyper-Threading
    - Disk space (hard drive/solid state): 64 GiB free space

## Not yet working

- Promiscuous mode (can manually configure in VirtualBox)
- Client VMs talking to the router VM directly (by default)
