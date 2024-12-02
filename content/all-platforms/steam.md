+++
title = 'Steam'
date = 2024-10-24T19:58:39+02:00
draft = false
+++

## Installation

### Windows

Go to the [Steam website](https://store.steampowered.com/about/), download and install Steam.

### Linux

Depending on your distribution and package manager, you need to run a different command in your terminal to install Steam.

Debian/Linux Mint/Ubuntu (be careful, recent versions of Ubuntu install the Snap version and [Steam developers recommend against it](https://mastodon.social/@TTimo/111772575146054328)).

```
sudo apt install steam
```

Arch-based distributions

```
sudo pacman -S steam
```

Fedora

```
sudo dnf install https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
sudo dnf install steam
```

Flatpak

```
sudo flatpak install steam
```

## Disable Remote Play

If you don't use this feature, you can disable it [from the settings](https://help.steampowered.com/en/faqs/view/0689-74B8-92AC-10F2#howdoidisableit). It won't run in the background this way.

## Configuring Proton (Linux only)

[Proton](https://github.com/ValveSoftware/Proton) is a tool forked from [Wine](https://www.winehq.org/) and developed by Valve to run Windows games on operating systems using Linux. It acts as a compatibility layer and you can enable it from the Steam settings.

You can check out [this guide made by GamingOnLinux](https://www.gamingonlinux.com/2019/07/steam-play-proton-guide-valves-tech-for-playing-windows-games-on-linux-steam-deck/) to configure it.

## Improve download speed (Linux only)

If Steam downloads are slower than normal, you can disable HTTP2 by running these commands inside a terminal:

```
echo "@nClientDownloadEnableHTTP2PlatformLinux 0" >> ~/.steam/steam/steam_dev.cfg
echo "@fDownloadRateImprovementToAddAnotherConnection 1.0" >> ~/.steam/steam/steam_dev.cfg
```
