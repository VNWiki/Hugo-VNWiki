+++
title = 'RPG Maker Games'
date = 2025-02-10T19:25:00+02:00
draft = false
+++
rpgmakermlinux-cicpoffs is a tool that allows you to play RPG Maker MV / MZ, RPG Maker XP, VX, VX Ace, MV, MZ, TyranoBuilder, Godot, Construct 2/3, and Nscripter games natively without using wine. It is mainly developed for RPG Maker games so the main compatibility is there. Most RPG Maker games do work with wine so you don't really need this, but some RPG Maker names has case-sensitive issues and this tool can reduce the time troubleshooting, with this you can start games from your right click menu or add it as a compatibility tool in Steam directly.

> [!info] Information
Github page: https://github.com/bakustarver/rpgmakermlinux-cicpoffs

## Install
Feel free to follow the instructions in the github page for more detailed instructions, but you can install it with this command:

`wget -qO- "https://raw.githubusercontent.com/bakustarver/rpgmakermlinux-cicpoffs/main/installgithub.sh" | bash`

> [!info] Information
To display all possible commands run: rpgmaker-linux --help


## Usage
### Terminal
`cd /path/to/game`

`rpgmaker-linux`

or 
`rpgmaker-linux --gamepath /path/rpg-maker-game/` (Be careful with spaces in the path)

### File Manager
Right click the game .exe and select open with: RPG Maker MV/MZ (cicpoffs mount)

![](https://i.imgur.com/1R2SrIA.png)

### Steam
If it's not a steam game first add it to steam as a non-steam game.

Right click > properties > compatibility > select RPG Maker MV/MZ (cicpoffs mount) Tool
![](https://i.imgur.com/RwRFlSU.png)


## Uninstall
Run the following command:

`wget -qO- "https://raw.githubusercontent.com/bakustarver/rpgmakermlinux-cicpoffs/main/uninstallgithub.sh" | bash`


