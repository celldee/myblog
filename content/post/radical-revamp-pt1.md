---
title: "Radical Laptop Revamp (Pt 1)"
date: 2017-07-07T11:53:51+01:00
draft: false
---

I have tried a number of Linux distros over the years and most recently was happily using Ubuntu 16.04 when I decided to give my laptop a complete revamp. Having read about tiling window managers a while ago, I had already installed [i3](https://i3wm.org/) and was pleased with the results. But then I read about [NixOS](https://nixos.org/) and [Wayland](https://wayland.freedesktop.org/) which prompted the thought - could I install NixOS and a Wayland window manager as the basis of a usable but stripped down set up?

At this point I should probably explain my choices of NixOS and Wayland. Well, I've been dabbling with [Clojure](https://clojure.org/) for a while now and it seems to me that immutability is a pretty useful property. NixOS is a Linux distro, based on the [Nix](https://nixos.org/nix/) package manager, that provides immutable and reproducible system builds allied with an interesting approach to dependency management. While NixOS was not easy to install, once I understood enough to be dangerous, it has provided me with a greater appreciation of how things work under the hood, mainly due to the declarative nature of the configuration.

Now, why Wayland? That was an easier decision. X is on its way out and the successor to the throne is Wayland. Now is as good a time as any to try to get to grips with it.

My motivation having been established, I took the plunge and went for NixOS 17.03 with the [Sway](http://swaywm.org) window manager, which is basically i3 on Wayland. My thinking was that I would use another laptop for the experiment, just in case I couldn't get something usable up and running in a reasonable amount of time. If I succeeded then I would make the NixOS laptop my day-to-day and if not, I would revert to my trusty Ubuntu workhorse.

Well, suffice it to say, I am writing this post on my NixOS laptop. No desktop environment in sight. Unity-less, Gnome-less, KDE-less. Just NixOS and Sway and some packages of my choosing managed by the Nix package manager.

OK, so what does my system look like?

![Screenshot](/image/screenshot.png)

It's not the prettiest I've ever seen, but it is functional and has the potential to allow me to work more efficiently than I have been thus far.

Here's a list of some of the software that I've installed, minus the languages and VM things like Java, Clojure, [golang](https://golang.org/) etc., to enable me to arrive at a comfortable set up:

* [Chromium](https://www.chromium.org/Home) - browser essential for my continued use of the Google eco-system
* [cmst](https://github.com/andrew-bibb/cmst) - QT gui for ConnMan
* [ConnMan](https://01.org/connman) - network manager
* [CUPS](https://www.cups.org/) - for printing
* [dmenu](http://tools.suckless.org/dmenu/) - dynamic menu for starting applications
* [i3blocks](https://github.com/vivien/i3blocks) - provides a flexible status bar
* [i3lock](https://github.com/i3/i3lock) - screen locker
* [imv](https://github.com/eXeC64/imv) - image viewer
* [irssi](https://irssi.org/) - irc client
* [Neovim](https://neovim.io) - editor
* [qutebrowser](https://www.qutebrowser.org/) - an interesting python-based browser with vim-like key bindings
* [ranger](http://ranger.nongnu.org/) - file manager with vi key bindings
* [Samba](https://www.samba.org/) - for Windows stuff
* [Sway](http://swaywm.org) - window manager
* [Terminology](https://github.com/billiob/terminology) - terminal emulator
* [VLC](https://www.videolan.org/index.html) - media player
* [Wayland](https://wayland.freedesktop.org/) - display server
* [XWayland](https://wayland.freedesktop.org/xserver.html) - compatibility layer for X clients
* [zathura](https://github.com/pwmt/zathura) - document viewer with vim-like key bindings

In subsequent posts I will go into more detail about the revamp, which is still a work in progress. There are things that I couldn't get working (and still haven't), and some hoops that I had to jump through.
