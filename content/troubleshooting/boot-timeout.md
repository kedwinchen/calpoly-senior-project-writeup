---
title: "Boot Timeout"
date: 2021-04-12T23:33:17-07:00
draft: true
---

```
Timed out while waiting for the machine to boot. This means that
Vagrant was unable to communicate with the guest machine within
the configured ("config.vm.boot_timeout" value) time period.

If you look above, you should be able to see the error(s) that
Vagrant had when attempting to connect to the machine. These errors
are usually good hints as to what may be wrong.

If you're using a custom box, make sure that networking is properly
working and you're able to connect to the machine. It is a common
problem that networking isn't setup properly in these boxes.
Verify that authentication configurations are also setup properly,
as well.

If the box appears to be booting properly, you may want to increase
the timeout ("config.vm.boot_timeout") value.
```

This is probably caused by [the current version of VirtualBox being incompatible with WSL]({{< relref "/troubleshooting/wsl" >}}).

This could also be due to resource exhaustion when the system is under higher load.
Running `vagrant up` again, even without closing some applications, may resolve this issue.

This may be similar to [this error]({{< relref "/troubleshooting/ssh-library-error" >}})
