+++
title = 'CDEmu'
date = 2024-10-22T07:37:38+02:00
draft = false
+++

CDEmu, or CDEmulation is needed to virtually mount your games on Linux for those pesky VNs without a digital version.

## Installation

### Steam Deck

> [!warning] Requirements
> SteamOS read-only mode disabled.

To disable read-only mode on your Steam Deck, run the following commands:

```
passwd # use this command only if you've never run the below command.
sudo steamos-readonly disable
```
If you make a mistake, simply press **CTRL + C** to cancel the command.

1. To install CDEmu on the Deck, just run these commands in the Konsole:

{{< tabs >}}
{{% tab title="SteamOS 3.5+" %}}
```
pacman-key --init # run these two commands if the below doesn't work
pacman-key --populate

sudo pacman -S linux-neptune-61-headers libmirage libao cdemu-client cdemu-daemon vhba-module-dkms

sudo modprobe vhba
```
{{% /tab %}}
{{% tab title="SteamOS 3.4 or before" %}}
```
pacman-key --init # run these two commands if the below doesn't work
pacman-key --populate

sudo pacman -S linux-neptune-headers libmirage libao cdemu-client cdemu-daemon vhba-module-dkms

sudo modprobe vhba
```
{{% /tab %}}
{{< /tabs >}}

When that’s finished running, and you’ve pressed **y** to everything, you’ll get a new menu to **Open with CDEmu client** when you right click certain files, or double click to open.

> [!info] Info
> If you don’t see any context menus, press F5 while in the folder of your game’s MDF/MDS/ISO files, and the icon should change.
> You can also refresh manually by clicking on the menu icon **☰** on the top right > More > View > Refresh.
> You may need to run this everytime SteamOS updates, or whenever it disappears, because the Steam Deck has an **immutable OS**.

## Usage

* Mount a disc image: `cdemu load 0 ~/image.iso`
* Unmount a disc image: `cdemu unload 0`

More information on the [CDEmu ArchWiki page](https://wiki.archlinux.org/title/CDemu)
