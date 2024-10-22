+++
title = 'Wineprefixes'
date = 2024-10-22T07:36:46+02:00
draft = false
+++

What is a Wineprefix?\
What is its function?\
What is a “clean” Wineprefix?

These are common questions, and here’s the answers to them

A WINEPREFIX is an environment variable.\
It defines where Wine looks for its configuration and files, in essence where it puts its C: drive.\
A clean prefix has no additional Windows components installed, often referred to as a vanilla wineprefix.

[Source](https://askubuntu.com/questions/956244/what-is-a-wineprefix)

Essentially, you can think of it like a mini Windows container.\
Wine makes a fake Windows container and does the translation between your Linux code & Windows instructions.\
A wine prefix is the folder (or directory, same word) that has the C:\ drive on your Linux system.\
And so, you can have multiple wine prefixes. This is what we’re going to do.

> [!info] Info
> On Linux, we like to have multiple wine prefixes that each do different things, and separate them because we don’t want their internal components to interfere with another, which can sometimes happen.


## How do I make a wineprefix?

### Main wineprefixes

Here are the main wineprefixes we’ll be needing to use for most cases.

1. Start by creating multiple folders called:
* lavfilters
* ffdshow
* wmp11
* xact
* wmp10
* wmp10quartz
* vanilla

You also can automate folder creation by using the console command (works on Steam Deck): `mkdir lavfilters ffdshow wmp11 xact wmp10 wmp10quartz vanilla`

> [!info] Info
> A vanilla wineprefix has nothing inside of it. You can skip step 3 for that wineprefix.

2. Next, we’ll setup each folder.

In Lutris, visit any game’s config and enter these settings

Game Options:
* **Wine prefix**: **path_to_your_wineprefix_folder**
* **Prefix architecture**: **64bit** (**32bit** for wmp10 & wmp10quartz)

Runner Options:
* **Wine version**: **Lutris 7.2 (default)**

> [!info] Info
> The **path** is the location of the folders we’ve just made.

> [!info] Info
> For developers who are lazy, enter the wineprefix field once in Lutris, then specify the wineprefix field before each command and append `&&` for each component command in the **Bash Terminal**.

3. Then, for each wineprefix folder, you’ll want these components depending on their name.
* Click the 🍷 wine bottle, and click **Bash Terminal**.
* Copy the command (based on the name of the prefix), paste it into each Terminal using **CTRL + SHIFT + V**
* Hit **Enter** to input the command.

> [!warning] Warning
> You must manually enable ALL codecs for **ffdshow** (including MPEG-1/2!) when the pop up occurs at the end of the install.

* **lavfilters** (64bit): `winetricks -q --force lavfilters d3dx9 dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015`
* **ffdshow** (64bit): `winetricks -q --force d3dx9 dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015 && winetricks ffdshow`
* **wmp11** (64bit): `winetricks -q --force wmp11 d3dx9 dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015`
* **xact** (64bit): `winetricks -q --force xact d3dx9 dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015`
* **wmp32** (32bit): `winetricks -q --force wmp10 d3dx9 dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015`
* **wmp32quartz** (32bit): `winetricks -q --force wmp10 d3dx9 dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015`

4. Next, within each wineprefix folder, install the [Windows Japanese Fonts](https://drive.google.com/file/d/1OiBgAmt3vPRu08gPpxFfzrtDgarBGszK/view).\
To install, place your fonts in **your_wineprefix/drive_c/Windows/Fonts**. This ensures your VNs can load the right font.\
Great! All the wineprefixes are now setup, except for **wmp10quartz** which needs special handling. You can skip this prefix if you don’t need it.

5. Get the [custom quartz files](https://www.visualnovelwiki.org/tutorials/wineprefixes/quartz2.zip). The .zip contains:
* quartz2.dll
* quartz2-win32.reg
* quartz2-win64.reg

> [!warning] Warning
> This archive also comes with quartz2-win64.reg, which can be used for 64 bit wineprefixes. **quartz2.dll** would also go in **drive_c/Windows/SysWow64** instead of **system32**. This wineprefix is using 32bit.

6. Find your wmp10quartz folder, and navigate to wmp10quartz/drive_c/Windows/system32\
Drag and drop the quartz2.dll file in there.

7. In Lutris, choose any game, and set the wineprefix to the wmp10quartz directory.\
* Game info
    * **Runner**, select **Wine**
* Game options
    * **Wine prefix**, set **wmp10quartz**’s folder path.
    * **Wine architecture**, set it to **32bit**

8. Save and click the 🍷 Wine Bottle, then select Bash Terminal.

9. Enter this command so we’re in the quartz2 folder:

```
cd <path-to-the-quartz2-folder-you-just-extracted>
# could be like this if in Downloads folder: cd ~/Downloads/quartz2
```

10. Enter this command to register the **quartz2.dll** file in the wineprefix (yhen close the **Bash Terminal**):

```
wine regsvr32 quartz2.dll
```

11. Click the 🍷 Wine Bottle again, then select Wine Registry. You’ll get a popup for the Windows Registry.

12. Click **Registry** in the **Toolbar** then **Import Registry File**. Find & import the **quartz2-win32.reg** file you downloaded.

Now you’re done! You can play most VNs now. Each VN page on the wiki should also have an install section or specify what wineprefix is needed.

## Special wineprefixes

For special games that require a certain prefix, i.e. Demonbane.

* demonbaneengine
* liarsoftengine
* yunoengine

In the [visual novel compatibility list](/all-platforms/visual-novel-compatibility-list), you might see: special: **wmp11** or whichever codec that’s specified. Please refer to the [special codec page](/linux/special-codecs) for those niche cases.

> [!info] Info
> The word "engine" here just refers to the name of the prefix, which is more intuitive and meaningful than just saying "wineprefix".

## Wine bugs/issues

> [!warning] Warning
> Installing quartz starting from Proton GE >= 7.20 won’t work. Still won’t work as of Proton GE 7.50. To get around this, use another Wine version/flavour before installing quartz.

> [!warning] Warning
> wmp11's 32bit installer is broken, but [we fixed it](https://github.com/Winetricks/winetricks/pull/1990). However, it’ll take some time before it gets downstreamed to a Wine version we can generally use. For now, we have to use a 64bit prefix (as of April 21 2023) with Lutris 7.2.

## Resources

### Windows Fonts

https://drive.google.com/file/d/1OiBgAmt3vPRu08gPpxFfzrtDgarBGszK/view
