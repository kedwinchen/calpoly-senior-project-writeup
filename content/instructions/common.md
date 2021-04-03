---
title: "Common Steps"
date: 2021-03-09T12:45:30-08:00
draft: true
---

## Software Installation

{{< details "Using a package manager (such as apt, dnf or brew)?" >}}

**ATTENTION PACKAGE MANAGER USERS**

Even though it may be tempting, it is strongly recommended to not use the
versions of Vagrant and/or VirtualBox that is available in your package
manager's repositories (e.g., using `apt install vagrant` or similar).
Using the following instructions below will ensure that the appropriate
versions of Vagrant and VirtualBox are installed.

If (**_and only if_**) you can guarantee that the versions for the software
available in your repositories are up-to-date with the latest versions available,
you may disregard this warning.

{{< /details >}}

### Linux Users

The following section will call for downloading either an `.rpm` or `.deb` file,
depending on your distribution.

- If you download a `.deb` file, install it using the following command(s):
  ```
  dpkg -i <path/to/where/you/saved/installer.deb>
  ```
- If you download a `.rpm` file, install it using the following command(s):
  ```
  rpm -ivh <path/to/where/you/saved/installer.rpm>
  ```
- If you download another file format, you probably know how to install it manually

If you need a refresher on what distribution you are using, execute `cat /etc/*release`

### Instructions

1. Install [Hashicorp Vagrant](https://www.vagrantup.com/downloads) by downloading the appropriate version for your operating system.

   - If you are on Debian/Ubuntu/Linux Mint or some other distribution that uses
     the `apt`/`dpkg` package manager, the "Debian" version should work (download the `.deb`)
   - If you are on Red Hat/CentOS/Fedora/Scientific Linux or some other
     distribution that uses the `dnf`/`yum`/`rpm` package manager, the "CentOS"
     version should work (download the `.rpm`)
   - If you must download the `.zip` file, `unzip` it and `install` the binary into somewhere in your `$PATH`

2. Install [Oracle VM VirtualBox](https://www.virtualbox.org/wiki/Downloads)

   1. Download the appropriate installer for your Operating System
   2. Use the installer as normal (or as described above, for Linux users)

3. Install VirtualBox Host Extension Pack

   1. [Download the VirtualBox Host Extension Pack](https://www.virtualbox.org/wiki/Downloads)
      (it is on the same page as VirtualBox download, just a bit further down the page)
   2. Open VirtualBox
   3. File -> Preferences
   4. `Extensions` tab
   5. Click `Add` (the button with the green "+" sign)
   6. Select the Extension Pack file
   7. Accept the Oracle Personal Use and Evaluation License (PUEL) when prompted
