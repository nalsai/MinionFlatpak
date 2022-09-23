# Minion Flatpak

📦 Flatpak Package of MMOUI Minion for Linux

Minion is a multi-platform application which allows users to browse, download, update and manage AddOns for supported games (Elder Scrolls Online and World of Warcraft).

Find out more about Minion on its website: <https://minion.gg/>

This Flatpak uses Azul's OpenJDK 8 Distribution with OpenJFX (ZuluFX) to run Minion natively on Linux.
A wrapper script allows the built-in updater to work by downloading updates to $XDG_DATA_HOME (`~/.var/app/gg.minion.Minion/data`) and running them from there.
The config files of minion are located in `~/.minion` because it doesn't respect the XDG Base Directory Specification (¬_¬").

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/repo/appstream/gg.minion.Minion.flatpakref
```

## Building

```bash
flatpak-builder --install-deps-from=flathub --force-clean build-dir gg.minion.Minion.yml
```
