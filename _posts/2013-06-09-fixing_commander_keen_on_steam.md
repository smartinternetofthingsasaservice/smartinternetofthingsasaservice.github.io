---
title  : Fixing Commander Keen on Steam
author : Jonas Schöley
date   : 2013-06-09
tags   : gaming tutorial
layout : post
---

[Commander Keen](https://en.wikipedia.org/wiki/Commander_keen). Great game, but with performance issues since I transitioned from Windows 7 to 8: Sluggish motion, stuttering sound...

Solution:

  1. Open the Dosbox `.conf` files for the game with a text editor. When you bought Keen on Steam the path reads as follows for the fourth game in the series: `...\Steam\SteamApps\common\Commander Keen\base4\keen4.conf`
  2. Change the entry `output` in section `sdl` to `openglnb`

I havn't had any luck with `ddraw` as output renderer, but with `openglnb` everything is running smooth.

This is how the `sdl` section in the `.conf` should look like after the change:

```cfg
[sdl]

fullscreen=true
fulldouble=true
fullresolution=800x600
windowresolution=original
output=openglnb
autolock=true
sensitivity=500
waitonerror=true
priority=higher,normal
mapperfile=mapper.txt
usescancodes=false
```

You will have to to this for every Keen game separately.

![](/assets/2013-06-09-fixing_commander_keen_on_steam/Dopefish.png)

cc-by Jonas Schöley