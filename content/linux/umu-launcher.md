+++
title = 'UMU Launcher'
date = 2024-10-24T19:18:55+02:00
draft = false
+++

[umu-launcher](https://github.com/Open-Wine-Components/umu-launcher) is a CLI tool to run applications with Proton outside Steam. It offers an easy access to a [unified online database](https://umu.openwinecomponents.org/) of game fixes called "protonfixes"

## Usage

Open a terminal emulator and run a command similar to:

```bash
WINEPREFIX=$HOME/Games/epic-games-store GAMEID=umu-dauntless PROTONPATH="$HOME/.steam/steam/compatibilitytools.d/GE-Proton8-28" umu-run "$HOME/Games/epic-games-store/drive_c/Program Files (x86)/Epic Games/Launcher/Portal/Binaries/Win32/EpicGamesLauncher.exe" -opengl -SkipBuildPatchPrereq
```

More examples are available in the [official documentation](https://github.com/Open-Wine-Components/umu-launcher/blob/main/docs/umu.1.scd) and in the [FAQ](https://github.com/Open-Wine-Components/umu-launcher/wiki/Frequently-asked-questions-(FAQ))
