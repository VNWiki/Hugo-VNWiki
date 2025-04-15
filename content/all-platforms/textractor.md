+++
title = 'Textractor'
date = 2024-10-24T20:07:15+02:00
draft = false
+++

[Textractor](https://github.com/Artikash/Textractor) (a.k.a. NextHooker) is an open-source x86/x64 video game text hooker for Windows 7+ (and Wine) based off of ITHVNR.

## Download

1. Download the zip version from github: https://github.com/Artikash/Textractor/releases/tag/v5.2.0
2. Unzip it in some location.
3. Update the dll from the alpha version for better compatibility: https://github.com/Artikash/Textractor/issues/868#issuecomment-1249146885
4. Alternatively, you can use Chenx221 fork instead of replacing dlls from alpha version: https://github.com/Chenx221/Textractor/releases It should have most if not all of alpha builds merged already.

## Linux 

Texthooking in Linux through wine is possible, it requires to run the texthooker software in the same wine prefix that the game.

### Lutris

1. Once you have your game running in Lutris the simplest way to run it is to right click the Lutris entry and click `Duplicate`
2. Change the name to identify it better.
3. Open the entry go to `Game Options` in Executable change to the textractor .exe ej: /home/user/Downloads/Textractor/x86/Textractor.exe
4. Run both the game and textractor, when clicking attach the game should appear normally.

> [!warning] Architecture
> The architecture x86 or x64 depends on what the game is running. When you try to attach it will either give an error message or crash if using wrong architecture.  
>
> It has no relation whatsoever with the wineprefix architecture. You can still hook 32 bit games in a 64 bit prefix.

> [!warning] Proton
> You have to use **Wine runners**, can't use proton with umu-launcher to texthook since they have extra containerized layer that blocks textractor from seeing other applications.
>
> As a workaround you can use [protonhax](https://github.com/Will40/protonhax/), it's extremely hacky though (you probably want to make a new Lutris entry with linux runner and run protonhax command)

> [!info] Gamescope
> If you wish to run the game with gamescope you will also need to run Textractor with gamescope, the steps are the same just enable gamescope in the new lutris entry for textractor, both should be run in fullscreen to avoid weird behaviour.
>
> Need to use Wayland and Wayland backend with gamescope (should be default already)
>
> You will also need a recent version of gamescope (tested with 3.16.3) since forwarding clipboard to the host was released [very recently](https://github.com/ValveSoftware/gamescope/pull/1685)
