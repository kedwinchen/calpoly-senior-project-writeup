---
title: "`vagrant halt` vs `vagrant destroy`"
date: 2021-04-07T17:25:11-07:00
draft: true
---

## What is the difference?

- `vagrant halt` turns off the Vagrant-managed VMs as defined in the `Vagrantfile`
- `vagrant destroy` deletes the Vagrant-managed VMs as defined in the `Vagrantfile`.
  **_This also deletes any files and configuration changes made to the VM._**

## When to use

- It is recommended to use `vagrant halt` when the VMs are not currently needed (e.g., at the end of a lab section), but will likely be needed again soon in order to free up computer resources.
- It is recommended to use `vagrant destroy` in the following situations:
  - When the VMs will no longer be needed moving forward (e.g., at the end of a quarter)
  - When VMs are in a bad or othwerise broken state
