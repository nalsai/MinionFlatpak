# Minion Flatpak

📦 Flatpak Package of MMOUI Minion for Linux

Minion is a multi-platform application which allows users to browse, download, update and manage AddOns for supported games (Elder Scrolls Online and World of Warcraft).

Find out more about Minion on its website: <https://minion.gg/>

This Flatpak uses Azul's OpenJDK 8 Distribution with OpenJFX (ZuluFX) to run Minion natively on Linux.
A wrapper script allows the built-in updater to work by downloading updates to $XDG_DATA_HOME (`~/.var/app/gg.minion.Minion/data`) and running them from there.

By default this Flatpak only has access to `~/Documents/Elder Scrolls Online/live/AddOns`, `~/.local/share/Steam/steamapps/compatdata/306130/pfx/drive_c/users/steamuser/Documents/Elder Scrolls Online` and `~/.var/app/com.valvesoftware.Steam/data/Steam/steamapps/compatdata/306130/pfx/drive_c/users/steamuser/Documents/Elder Scrolls Online`.  
You can grant access to other directories using Flatseal or by running `flatpak override --filesystem=/path/to/directory gg.minion.Minion`

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/repo/appstream/gg.minion.Minion.flatpakref
```

## Building

```bash
flatpak-builder --install-deps-from=flathub --force-clean build-dir gg.minion.Minion.yml
```
