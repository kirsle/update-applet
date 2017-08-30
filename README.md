# Update Applet

![Screenshot](https://raw.githubusercontent.com/kirsle/update-applet/master/screenshot.png)

This is a Python GTK+ app that notifies you about available updates on
RedHat-like operating systems, such as Fedora and CentOS (with the `dnf` or
`yum` package managers).

This app is useful for desktop environments such as Xfce that no longer have a
native option for notification updates: after GNOME integrated their own
update notifier, the other desktop environments have been left to fend for
themselves.

I wrote it to scratch my own itch and it used to live in my personal
dotfiles repo, but now it has its own repo where it can be more easily
discoverable by others.

# Current Status/To Do

I've pulled the script out of my dotfiles and put it here. It will need some
more work done soon:

* Make it easy to configure. Currently you have to edit the source to change
  settings.
* Make it automatically detect `dnf` and `yum` with a preference for `dnf`.
  Currently it only deals with `dnf` for modern Fedora systems.
* Investigate getting it to work with sudoless `apt` commands for Debian-based
  systems.

# Installation

Copy the `update-applet` script into your `~/bin` or somewhere on your `$PATH`.
To automatically start the program on Xfce or MATE desktop environments, copy
the example autostart config into your `~/.config/autostart/` folder.

See `update-applet --help` for help. If you don't have any updates pending and
want to verify the applet works, run it with the `--testing` or `-t` parameter,
like `update-applet -t`. This will force the notification icon to display as
though updates are available.

# License

The MIT License (MIT)

Copyright (c) 2017 Noah Petherbridge

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
