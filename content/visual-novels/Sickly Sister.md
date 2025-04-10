+++
title = 'Sickly Sister - Koshikiyukashii Byoujaku Imouto'
date = 2025-02-10T20:11:58+01:00
draft = false
+++

## Installation

### Linux

> [!info] Information
> This game uses a borked implementation of Direct2D in Wine, need to to use a [d2d1 wrapper](https://cdn.discordapp.com/attachments/1014276025728901197/1359424015994847372/d2d1.dll?ex=67f76dc6&is=67f61c46&hm=497d45b9f170a46c590adb2f514ccca942997985fb2144c8f7c5c7a893b2e122&) made specifically for the game (Thanks to @fission)
> Tested with [Proton-ge 9.26+](/linux/adding-wine-versions).


#### Steps

1. Add the downloaded [d2d1.dll](https://cdn.discordapp.com/attachments/1014276025728901197/1359424015994847372/d2d1.dll?ex=67f76dc6&is=67f61c46&hm=497d45b9f170a46c590adb2f514ccca942997985fb2144c8f7c5c7a893b2e122&) to the game folder, at the same level than the .exe to run the game

2. In lutris add a new entry:

* Game options:
    - Executable: Add the executable to the game.exe
    - wine prefix: use [wmp11 prefix]({{< ref "Wineprefixes" >}}).
* Runner Options:
    - Wine Version: Proton or wine both work, tested with proton-ge 9.26, but any modern version should work.
    - DLL overrides: key: `d2d1` value: `n,b`


You can also do the DLL override accesing winecfg of the prefix:
![](https://cdn.discordapp.com/attachments/1014276025728901197/1359330990350401637/d2d1override.png?ex=67f71723&is=67f5c5a3&hm=8ffbf197fdfb58d16fe59335b70fbcb03871e4da495310e8f350ccdee29da563&)


## Links

* [VNDB](https://vndb.org/v48724)
