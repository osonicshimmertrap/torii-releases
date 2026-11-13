# Torii releases

Downloads of **Torii**, a macOS menu bar app for GlobalProtect VPNs: one
click to connect, and only the destinations you choose go through the
tunnel.

This repository holds the packages and the list of versions that
installed copies read when you ask them to update. It holds no source
code.

## Download

Get the newest disk image from
[Releases](https://github.com/osonicshimmertrap/torii-releases/releases/latest).

## Requirements

- macOS 26 or later, on Apple Silicon
- An administrator account on the Mac, for a one-time set-up step
- A GlobalProtect gateway that accepts a username and password

## Install

Torii is not signed with an Apple Developer ID, so macOS asks for an
extra approval the first time.

1. Open the disk image and drag **Torii** to **Applications** in Finder.
   Do not run it from the disk image or the Downloads folder.
2. Open Torii. macOS blocks it. Open **System Settings -> Privacy &
   Security**, scroll to the message about Torii, and press **Open
   Anyway**.
3. Click the gate in the menu bar and fill in the profile: a name, the
   gateway's host name, your username and your password.
4. Press **Set up** and enter your Mac password. This installs Torii's
   helper and VPN engine and approves the gateway.
5. Press **Connect**.

## Updating

Torii checks once a week, when it is opened, whether a newer version
exists, and tells you. It installs an update only when you press
**Install update** on its Updates screen. Before anything is replaced,
the package is checked against a key built into Torii, so only packages
made by Torii's author are accepted.

After an update macOS may ask once whether Torii may use the saved
password (choose **Always Allow**), and Torii may ask for your Mac
password to update its helper.

## What Torii sends

- **Once per version:** that a copy was installed or updated, with the
  Torii version and the macOS version. No identifier.
- **Once a week, and when you ask:** a question, "which version is the
  latest?", that carries nothing.
- **When you install an update:** a download from this repository.

Torii never sends your gateway, username, routes, host names, profile
names, session times or log. It counts copies, not people. Both the count
and the weekly check can be switched off on Torii's Updates screen.

## Licence

Torii is released under the [Functional Source License, Version 1.1, MIT
Future License](LICENSE.md). It bundles OpenConnect, GnuTLS and other
libraries under the GNU Lesser General Public License and similar
licences, and the Sparkle updater under the MIT licence; their licence
texts are inside the app.
