+++
title = 'Adding icons on GNOME'
date = 2024-10-22T07:37:20+02:00
draft = false
+++

If you use the GNOME desktop environment, you might have [trouble with custom desktop entries](https://github.com/ValveSoftware/steam-for-linux/issues/11012). To fix them, add `StartupWMClass` at the end of your entries and set the value to the output of `xprop`, `lg` or `wlprop`.
