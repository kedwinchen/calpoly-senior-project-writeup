---
title: "macOS has errors..."
date: 2021-03-29T10:43:10-07:00
draft: true
---

{{< hint info >}}
**_Note:_** This guide was developed on a Linux-based OS, and tested on both Linux-based and Windows. The (original) writer did not (and probably still does not) have access to a macOS device. Please report any errors/bugs not listed here to Kedwin Chen <a href="mailto:kchen75@calpoly.edu?subject=[CPE 462] macOS Error">kchen75@calpoly.edu</a>, and include `[CPE 462] macOS Error` in the subject line.
{{< /hint >}}

## `/dev/vboxnetctl`: no such file or directory

This is likely due to newer macOS versions blocking Kernel Extensions. To resolve, perform the following steps:

1. Perform the shutdown procedure ([documented here]({{< relref "/instructions/students" >}}))
2. Run the following command

```bash
sudo "/Library/Application Support/VirtualBox/LaunchDaemons/VirtualBoxStartup.sh" restart
```

3. There will likely be a prompt regarding Kernel Extensions, click "Allow" when prompted.
   Also check **System Preferences** -> **Security and Privacy** to ensure that VirtualBox
   (may be listed as **Oracle VirtualBox** or similar) has the required permissions.
4. Save any open work, and restart the computer to ensure that the changes take effect.
