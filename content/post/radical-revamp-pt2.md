---
title: "Radical Laptop Revamp (Pt 2)"
subtitle: "Installing NixOS"
date: 2017-07-09T11:52:20+01:00
draft: false 
---

This is the second of my "Radical Revamp" posts. The following are the steps that I took to install NixOS 17.03:

1. Find some useful information. For me, the [NixOS manual](https://nixos.org/nixos/manual/) and [this gist](https://gist.github.com/martijnvermaat/76f2e24d0239470dd71050358b4d5134) were my main resources.

2. Download a version of NixOS from the download page. I chose the 'Graphical Live CD' so that I could get an impression of what a working NixOS set up looked like.

3. Create a bootable USB from the downloaded image.

4. Partition the hard drive(s). This is a manual process and I followed the partition scheme described in the gist mentioned above, including LUKS encryption.

5. Mount partitions.

6. Make sure that WiFi is working so that downloads can be performed during installation.

7. Generate NixOS configuration file and modify it as required.

8. Install NixOS by running the `nixos-install` command and then reboot.

If all goes according to plan then you should be able to boot into a basic console.

In the next post I will describe what I had to add to the **configuration.nix** file to get things like the touchpad working and how I configured [Sway](http://swaywm.org) to get my minimal desktop.
