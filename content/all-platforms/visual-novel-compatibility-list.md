+++
title = 'Visual novel compatibility list'
date = 2024-10-21T19:33:37+02:00
draft = false
+++

A brief overview **on what works** for a Visual Novel and its confirmed working platforms.

* ✅ Verified to work
* ⚠️ Playable, with some issues
* ❓ Unknown
* N/A Not applicable

If you are experiencing font issues, be sure to install the Windows Japanese Fonts. Common examples are MS Gothic, Mincho, etc.

| Visual Novel | Windows | Mac | Linux | Steam Deck | Game engine | Wineprefix   | Wine version           | Notes                                                                                                                                         |
|:--------------:|:---------:|:-----:|:-------:|:------------:|:-------------:|:--------------:|:------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| Tsukihime    | ✅       | ✅   | ✅     | ✅          |             | vanilla(any) | any                    | abandonware;   can be played on a browser - https://tsukiweb.holofield.fr/   or offline, using the original exe - https://www.readtsukihi.me/ |
| DRACU-RIOT!  | ✅       | ❓   | ✅     | ✅          | KiriKiri    | wmp10quartz  | Proton 7+              | Disable `Esync`                                                                                                                               |
| Riddle Joker | ✅       | ❓   | ✅     | ✅          | KiriKiri    | wmp10quartz  | Lutris 7.2+  Proton 7+ | Disable `Esync` |
| Kinkoi: Golden Loveriche | ✅       | ❓   | ✅     | ✅          | KiriKiri | vanilla(any) | Proton GE 7.43+ | Add “WINE_DO_NOT_CREATE_DXGI_DEVICE_MANAGER=1 %command%” OP/ED work out of the box | Meteor World Actor: Badge & Dagger | ✅       | ❓   | ✅     | ✅          | Artemis | vanilla |  Proton GE 8.6+ | Add "GST_PLUGIN_FEATURE_RANK=protonaudioconverterbin:NONE %command%" to be able to play the OP |
| A Clockwork Ley-Line: Flowers Falling in the Morning Mist | ✅       | ❓   | ✅     | ✅          | | vanilla | Proton 7.0+ | Add “PROTON_USE_WINED3D=1 LANG="ja_JP.UTF-8"  %command%” on launch options on steam, if not, you will get stuck on a white screen when the OP start |
| Kamidori Alchemy Meister | ✅       | ❓   | ✅     | ✅          | | wmp10quartz | Lutris 7.2+ Proton 7.0+ | JP Locale Enabled Runs a little laggy in wine8, but is smoother in lutris 7.2.2 . Will experiment more. | 
| Neko Nights | ✅       | ❓   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7.0+ | JP Locale enabled |
| Senren＊Banka | ✅       | ❓   | ✅     | ✅          | KiriKiri | Special: wmp11 | Lutris 5.13+ Proton GE 8.8+ | Disable Esync
| True Remembrance | ✅       | ✅   | ✅     | ✅          | | N/A | N/A | has Native Mac/Linux version (2x version)
| Majikoi! Love Me Seriously! | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Dies irae ~Amantes amentes~ | ✅       | ✅   | ✅     | ✅          | Malie | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Maitetsu Last Run! | ✅       | ❓   | ✅     | ❓          | KiriKiri | wmp11 | Proton GE 7.31+ | Switch Kirikiri advanced options to use “Layer” |
| Tsukihime -A piece of blue glass moon- | ✅       | ✅   | ✅     | ✅          | Kirikiri | N/A | N/A | Run the switch version on Ryujinx to avoid sprite lag. |
| Gnosia | ✅       | ❓   | ✅     | ❓          | | N/A | Proton GE 8-6 |
| Forest | ✅       | ❓   | ✅     | ❓          | codeX RScript | liarsoftengine / special: mciqtz32 | Lutris 7.21+, Proton 7+ | Not yet tested, but liarsoftengine should work. |
| Harmonia | ✅       | ✅   | ✅     | ✅          | Siglus Engine | lavfilters | Lutris 7.21+ Proton 7+ | |
| G-Senjou no Maou - The Devil on G-String | ✅       | ✅   | ✅     | ✅          | Kirikiri | wmp10quartz | Lutris 7.21+ Proton 7+ | |
| Utawarerumono: Prelude to the Fallen | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | 
| Utawarerumono: Mask of Deception | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ |
| Dōkyūsei: Bangin' Summer (remake) | ✅       | ✅   | ✅     | ✅          | | lavfilters | Proton GE 7.31+ | Graphical glitches on default wine |
| Fureraba ~Friend to Lover~ | ✅       | ✅   | ✅     | ✅          | | lavfilters | Lutris 7.21+ Proton 7+ | HD renewal edition |
| Utawarerumono: Mask of Truth | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Utawarerumono (2002, original) | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Saku Saku: Love Blooms with the Cherry Blossoms | ✅       | ✅   | ✅     | ✅          | | lavfilters / ffdshow | Proton GE 7.20+
| Spirit Hunter: Death Mark | ✅       | ❌   | ❌    | ❌          | | ❌ | ❌ | borked for now, untested for Proton 8 (https://www.protondb.com/app/980830) |
| Umineko - When They Cry | ✅       | ✅   | ✅     | ✅          | NScripter | vanilla (any) | Lutris 7.21+ Proton 7+ | w/ witch hunt translations. For HD sprite/PS3 version port, see Umineko Project (supported). The original japanese release might require deleting some fonts from the wineprefix as nscripter defaults to a font on its own and there are no options to select one |
| Higurashi - When They Cry | ✅       | ✅   | ✅     | ✅          | NScripter | vanilla (any) | Lutris 7.21+ Proton 7+ | w/ witch hunt translations. The original japanese release might require deleting some fonts from the wineprefix as nscripter defaults to a font on its own and there are no options to select one. |
| Spirit Hunter: NG | ✅       | ❌   | ⚠️    | ⚠️         | | N/A | Proton 7+ | movies don't play, but otherwise semi-playable. untested for Proton 8 (https://www.protondb.com/app/1100430) |
| Your Turn To Die -Death Game By Majority- | ✅       | ❓   | ✅     | ✅          | | ❓ | ❓ | input lag on some linux devices, possible lag when loading an asset. Applicable to all rpg maker mv/mz games.  |
| MUSICUS! | ✅       | ❓   | ✅     | ❓          | | ffdshow | Lutris 7.21+ Proton 7+ | not yet tested. movies if any? |
| Clannad | ✅       | ✅   | ✅     | ✅          |  RealLive |  wmp10quartz | Lutris 7.21+ Proton 7+ | |
| Majikoi A-1 | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | JP Locale enabled |
| Majikoi A-2 | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | JP Locale enabled |
| Majikoi A-3 | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | JP Locale enabled |
| Majikoi A-4 | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | JP Locale enabled |
| Majikoi S | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | JP Locale enabled |
| Dead End Aegis Dead End Aegis Gaiden | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ |  |
| YOU and ME and HER: A Love Story (totono) | ✅       | ✅   | ✅     | ✅          | N2System N4System(JAST) | lavfilters/ffdshow + xact | Lutris 7.21+ Proton 7+ | Install xact with lavfilters or ffdshow |
| Katawa Shoujo | ✅       | ✅   | ✅     | ✅          | | N/A | N/A | has Native Mac/Linux version |
| Baldr Sky | ✅       | ✅   | ✅     | ✅          | | lavfilters | Lutris 7.21+ Proton 7+ | Lutris 7.21+ Proton 7+ | Opening video & audio desync fixed by setting FPS limiter to 30 or `gamescope --framerate 30 BaldrSky.exe` |
| Sabbath of the Witch | ✅       | ✅   | ✅     | ✅          | kirikiri | special: wmp11 | Lutris 7.21+ Proton 7+ | Disable DXVK Press ALT for Advanced Settings > Movie Rendering > Layer |
| Cyanotype Daydream | ✅       | ✅   | ✅     | ✅          | |wmp10quartz | Lutris 7.21+ Proton 7+ | |
| White Album 2 Introductory Chapter & Closing Chapter | ✅       | ✅   | ✅     | ✅          | |wmp10quartz / special: wmp11quartz | Lutris 7.21+ Proton 7+ | requires special install. d3d9 set override n,b |
| Fruit of Grisaia | ✅       | ✅   | ⚠️     | ⚠️          | CatSystem2 | wmp10quartz | Lutris 7.21+ Proton 7+ | Movies flicker, but otherwise fully playable. |
| Labyrinth of Grisaia | ✅       | ✅   | ⚠️     | ⚠️          | CatSystem2 | wmp10quartz | Lutris 7.21+ Proton 7+ | Movies flicker, but otherwise fully playable. |
| Eden of Grisaia | ✅       | ✅   | ⚠️     | ⚠️          | CatSystem2 | wmp10quartz | Lutris 7.21+ Proton 7+ | Movies flicker, but otherwise fully playable. |
| Persona 5 Royal | ✅       | ❌   | ✅     | ✅          | | any | Lutris 7.21+ Proton 7+ | Steam Deck: 1920x1080 resolution override in Steam Game Properties, 40 fps lock. |
| Yosuga no Sora | ✅       | ✅   | ✅     | ✅          | | any | Lutris 7.21+ Proton 7+ | JP Locale enabled |
| Saya no Uta (original) | ✅       | ✅   | ✅     | ✅          | nps | lavfilters | Lutris 7.21+ Proton 7+ | |
| Saya no Uta (remaster) | ✅       | ✅   | ✅     | ✅          | N4System | xact | Lutris 7.21+ Proton 7+ | |
| YU-NO PC-95 (w/ Voice Mod & BGM Mod) | ✅       | ✅   | ✅     | ✅          | | yunoengine | Lutris 7.21+ Proton 7+ | requires special install. |
| Corpse Party (2021) | ✅       | ✅   | ✅     | ✅          |  | any | Lutris 7.21+ Proton 7+ | |
| eden* They were only two, on the planet. | ✅       | ✅   | ✅     | ✅          |  | lavfilters | Lutris 7.21+ Proton 7+ | |
| Evenicle 1 | ✅       | ✅   | ✅     | ✅          | | any | Lutris 7.21+ Proton 7+ | MUST HAVE game version 1.04: turn on full screen mode, and enable compatibility mode in in-game config. |
| Evenicle 2 | ✅       | ✅   | ✅     | ✅          | |any | Lutris 7.21+ Proton 7+ | |
| ef - the first tale. | ✅       | ✅   | ✅     | ✅          | | lavfilters | Lutris 7.21+ Proton 7+ | |
| ef - the latter tale. | ✅       | ✅   | ✅     | ✅          | | lavfilters | Lutris 7.21+ Proton 7+ | |
| Never7 -the end of infinity- | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | any | love2D engine required (has native windows/linux ver) |
| Ever17 -the out of infinity- HIMMEL Edition | ✅       | ⚠️   | ⚠️     | ⚠️          | | vanilla / lavfilters | any | Requires special install.Set the virtual resolution to 800x600 to correctly crop the videos. |
| Remember11 -the age of infinity- GESTALT edition | ✅       | ✅   | ✅     | ✅          | | lavfilters | any | |
| StarTrain | ✅       | ✅   | ⚠️     | ✅          |  Kirikiri | wmp10quartz | Lutris 7.21+ | Fullscreen does not work, but fixable with Gamescope. Disable DXVK |
| Steins;Gate | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | w/ COZ patch |
| Steins;Gate 0 | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | w/ COZ patch |
| Tsui no Stella | ✅       | ✅   | ✅     | ✅          | Siglus Engine | wmp10quartz / wmp11 | Lutris 7.21+ | See guide to choose which prefix needed. Disable DXVK. |
| Root Double | ✅       | ❓   | ⚠️     | ⚠️          | | vanilla (any) | any | Font rendering is low quality on Unix systems |
| Deus Machina Demonbane | ✅       | ✅   | ✅     | ✅          | N2System | demonbaneengine | Lutris 7.21+ Proton 7+ | |
| Subarashiki Hibi ~Furenzoku Sonzai~ | ✅       | ✅   | ✅     | ✅          | BGI | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Baldr Heart + EXE | ✅       | ✅   | ✅     | ⚠️         | NeXAS | wmp10quartz | Lutris 7.21+ Proton 7+ | Severe frame drops when high enemy count in the Steam Deck on later stages. |
| Full Metal Daemon: Muramasa | ✅       | ✅   | ✅     | ✅          | N2System/N4System (JAST) | muramasaengine | Lutris 7.21+ Proton 7+ |
| AIR | ✅       | ✅   | ✅     | ✅          | RealLive | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Fate/stay night | ✅       | ✅   | ✅     | ✅          | Kirikiri | lavfilters / wmp10quartz | Lutris 6.21+ Proton 7+ | |
| Gore Screaming Show | ✅       | ❓   | ✅     | ✅          | | lavfilters | Lutris 7.21+ Proton 7+ | |
| Hoshi Ori Yume Mirai | ✅       | ✅   | ✅     | ✅          | Siglus Engine | vanilla (any) | lutris-GE-Proton-7-32+ | |
| Ima Sugu Onii-chan ni Imouto da tte Iitai! | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Kanon | ✅       | ✅   | ✅     | ✅          | RealLive | vanilla (any) | Lutris 7.21+ Proton 7+ | |
| Muv-Luv | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | lutris-GE-Proton-7-21+ | |
| Muv-Luv Alternative | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | any | |
| Kana ~Imouto~ | ✅       | ❓   | ✅     | ✅          | | wmp10quartz | Lutris 7.2+ | |
| Otome wa Boku ni Koishiteru | ✅       | ❓   | ✅     | ✅          | | wmp10quartz | Lutris 7.2+ | |
| Sakura no Toki | ✅       | ❓   | ✅     | ✅          | Artemis | artemisengine | Lutris 7.2+ | Use Gamescope/Game mode to avoid video flickering |
| Sakura no Uta | ✅       | ❓   | ✅     | ✅          | BGI | lavfilters / wmp10quartz | Lutris 7.2+ Proton GE 8-13+ | JP Locale Enable Spanish translation works but some characters like “ñ” or letters with accents don't appear
| Albatross Koukairoku | ✅       | ✅   | ✅     | ✅          | codeX RScript  | liarsoftengine / special: mciqtz32 | Lutris 7.2+ | |
| Gahkthun of the Golden Lightning -What a Radiant Brave- | ✅       | ✅   | ✅     | ✅          | codeX RScript  | liarsoftengine / special: mciqtz32 | Lutris 7.2+ | |
| Ayakashibito | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.2+ | uses modified aya.bat script to run game |
| Umineko Project | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | any | Has Native Linux version.
| Kara no Shoujo | ✅       | ✅   | ✅     | ✅          | InnocentGrey engine Kirikiri (mangagamer) | vanilla (any) | any | |
| Kara no Shoujo (HD) | ✅       | ✅   | ✅     | ✅          | InnocentGrey engine | wmp11quartz | Lutris 7.2+ Proton 7+ | Make sure patch is up to date. d2d1 override set to n,b or in winecfg |
| Kara no Shoujo 2 | ✅       | ✅   | ✅     | ✅          | InnocentGrey engine Unity (mangagamer) | N/A | N/A | Has native Mac & Linux version. |
| Tokyo Babel | ✅       | ✅   | ✅     | ✅          | | vanilla (any) | Lutris 7.2+ | |
| Saihate no Ima | ✅       | ✅   | ✅     | ✅          | | wmp10quartz / liarsoftengine | Lutris 7.2+ | disable DXVK. needs font in the prefix to avoid startup crash. sometimes the op video crashes if left to play to the end click to skip before it ends naturally |
| Kikokugai The Cyber Slayer | ✅       | ❓  | ⚠️     | ❓          | nps N2System (remake) | vanilla | Proton GE 7.20+ | Broken formatting in the textbox on linux. Still in a readable state. |
| Hatsukoi 1/1 | ✅       | ❓  | ✅     | ✅          | Siglus Engine | vanilla | Proton GE 7.32 | |
| Sakuranomori Dreamers | ✅       | ❓  | ✅     | ✅          | | vanilla | Proton GE 7.43 | |
| Shin Koihime † Musou ~Otome Ryouran ☆ Sangokushi Engi~ | ✅       |   | ✅     | ✅          | | lavfilters | Proton GE 7.16 | Interface is in Japanese |
| Ore-tachi ni Tsubasa wa Nai | ✅       | ❓  | ✅     | ❓          | Lucifen | wmp11 + quartz_dx | Lutris 7.2 | Disable DKVX use special codecs: `sh codec.sh wmp11 quartz-dx` |
| Hello;World | ✅       | ❓  | ✅     | ❓          | nps | wmp11 + quartz_dx | Lutris 7.2 | Disable DKVX use special codecs: `sh codec.sh wmp11 quartz-dx` |
| Nukige Mitai na Shima ni Sunderu Watashi wa Dou Surya Ii Desu ka? | ✅       | ❓  | ✅     | ❓          | Shiina Rio | vanilla | Lutris 7.2 | |
| Kishin Houkou Demonbane  | ✅       | ❓  | ✅     | ✅          | N4System | muramasaengine + xact | Lutris 7.2 | English fantl has wordwrapping issues in linux. Japanese works fine. |
| Sore wa Maichiru Sakura no You ni -Re:BIRTH- | ✅       | ❓  | ✅     | ✅          | Artemis | vanilla wine-ge/proton-ge | Lutris GE-proton 8.14 | |
| GINKA | ✅       | ❓  | ✅     | ✅          | Kirikiri | wmp11quartz |  Lutris 7.2 | |
| Rewrite | ✅       | ❓  | ✅     | ✅          | Siglus engine | wmp10quartz(Japanese version) | Lutris 7.2 | Lutris 7.2 	English version should work by default in Steam. Japanese version requires wmp10quartz (wmp11quartz does not work) install quartz manually as the script does not work here for 32bit |
| Clover Day's Plus | ✅       | ❓  | ✅     | ✅          | Kirikiri/Unity | kirikiri → wmp11quartz_dx Unity → wine-ge/proton-ge | kirikiri → Lutris 7.2 Unity → wine-ge 8.22 | If running the new Unity version in lutris make sure to enable DKVX. Otherwise disable. |
| Sousaku Kanojo no Ren'ai Koushiki | ✅       | ❓  | ✅     | ✅          | Kirikiri | wmp11quartz | Lutris 7.2 | Disable DKVX |
| Tenshi no Nichou Kenjuu -Angelos Armas- | ✅       | ❓  | ✅     | ✅          | nps | wmp11 + quartz_dx | Lutris 7.2 | Disable DKVX use special codecs: `sh codec.sh wmp11 quartz-dx` Seems to crash on 32 bit prefixes and some wine versions |
| Moshimo Ashita ga Hare Naraba |  ✅       | ❓  | ✅     | ✅          | | wmp11 + quartz_dx | Lutris 7.2 | Disable DKVX use special codecs: `sh codec.sh wmp11 quartz-dx` | 
| Geminism |  ✅       | ❓  | ✅     | ✅          | Unity | vanilla with wine-ge | Lutris-ge-proton 8.23 | |

