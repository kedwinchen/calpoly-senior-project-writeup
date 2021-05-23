---
title: "Home"
date: 2021-03-09T12:35:47-08:00
draft: true
---

This site is a living\* write-up for my senior project, Project (TODO: name the project).

## What?

Using Vagrant + VirtualBox to create consistent, distributable lab environments.

## Why?

See the [features list]({{< relref "faq/features" >}}) (more reasons below)

### Why not the `unix*.csc.calpoly.edu` servers?

- Requires GlobalProtect VPN (without split-tunneling, can be considered an invasion of privacy)
- Difficult (or annoying) to constantly sync files for rapid develop/test cycles
- Cannot (easily) run multiple instances of privileged services (e.g., one instance of `mysql` for each student)
- Cannot run graphical applications (note: this project does not (and cannot) automagically provide a solution for workloads requiring GPU/hardware acceleration)
- Other minor quality-of-life things I cannot think of at this time

### Limitations

- May require somewhat recent and/or powerful hardware (i.e., may not run on Chromebooks) (most hardware released within the past 5-10 years should suffice!)
- Creates another set of troubleshooting issues
- Can not automagically provide a solution for workloads requiring GPU/hardware acceleration
- May not be able to provide Windows-based VMs due to licensing restrictions (more research/legal counsel needed)

## Genesis

This project idea originally came to me as I was working with the [Cal Poly Security Education Club](https://cpsecurity.club)
(formerly known as Cal Poly White Hat) to devise a method to have a common environment for CTF events,
with tools set up so helping students remotely would be simpler (to save time debugging environment inconsistencies issues).

This expanded to helping professors with distributed lab environments.
The first course to adopt this was Dr. DeBruhl's [CSC 422]({{< relref "/courses/csc-422" >}}) course.
It had a set of very specific requirements (multiple virtual machines, special networking setup), and is a good example of the capabilities of this project.

## Other Challenges

Relevant XKCD:

![https://imgs.xkcd.com/comics/standards.png](https://imgs.xkcd.com/comics/standards.png "https://xkcd.com/927/")

Source: [https://xkcd.com/927/](https://xkcd.com/927/)
