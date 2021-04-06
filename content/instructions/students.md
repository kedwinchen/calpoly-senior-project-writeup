---
title: "Students (End Users)"
date: 2021-03-09T12:25:30-08:00
draft: true
---

## Setting up the environment

1.  Follow the [common procedures]({{< relref "./common" >}})
2.  Obtain the `Vagrantfile` for the course

    Note: Vagrant requires that the Vagrantfile does not have an extension.
    Some browsers may try to save the Vagrantfile as "Vagrantfile.txt" -- this will not work.
    You may need to manually remove the extension
    (saving as type "All Files" instead of "Text Document" often resolves this issue.)

3.  Using a terminal, navigate to the folder you saved `Vagrantfile` to
4.  Run `vagrant up`
5.  After the command completes, the virtual machine(s) should be brought up.
6.  After you are done with the graphical session, close the window. Be sure to select "Continue running in the background" when prompted

## Using the environment

### Logging in to the VMs

{{< hint danger >}}
Save all data you wish to keep into `/vagrant`.
This is the only directory whose contents are not deleted when the VM is destroyed.
{{< /hint >}}

#### Using `ssh`

1.  Using a terminal, navigate to the folder you saved `Vagrantfile` to.
2.  run `vagrant ssh`
3.  The default user is (usually) `vagrant` and has a password of `vagrant`.
4.  This user should be able to run commands as `root` (using `sudo`) without asking for a password.

#### Direct GUI/Console Access

1. To obtain a graphical console to a VM, open `Oracle VM VirtualBox` (will likely be in your "Start Menu" or "Launchpad" or similar)
2. Select the VM you would like to connect to
3. Click on the "Show" button (the green arrow on the top bar)
4. If prompted for login credentials, the default username and password are both `vagrant`

### Shutting down the VMs

{{< hint warning >}}
Do not directly manipulate machine state using VirtualBox!!
Doing so could leave Vagrant in an unpredictable state.
{{< /hint >}}

{{< hint danger >}}
Save all data you wish to keep into `/vagrant`.
This is the only directory whose contents are easily accessible when the VM is powered off.
{{< /hint >}}

1. Using a terminal, navigate to the folder you saved `Vagrantfile` to.
2. Run `vagrant halt`

## Tearing down the environment

{{< hint warning >}}
Do not directly delete virtual machines using VirtualBox!!
Doing so could leave Vagrant in an unpredictable state.
{{< /hint >}}

1. Using a terminal, navigate to the folder you saved `Vagrantfile` to.
2. Use `vagrant destroy` to destroy all VMs and administrative data that Vagrant generated.
3. Confirm when prompted (alternatively, provide `-f` option to `vagrant destroy`)
